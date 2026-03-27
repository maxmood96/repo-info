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
$ docker pull fluentd@sha256:b48a22c6359bd460092ae16029c2367e65298eb946f9f0d6731aa8c168185fd1
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
$ docker pull fluentd@sha256:232406cf7372ec3334cc854604c6e4da073278562f45b4f4ba1999c1b0bdcb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79239187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160b4477cbc5df32a10ae2e9d2c1d4ace19b5e42149b80e2f51aebd182a1e0c8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:27:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:27:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:27:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:27:58 GMT
USER fluent
# Tue, 17 Mar 2026 00:27:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:27:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c59864e0006c1e4962cbce8eefb3283a4a8eb888aab9f56e43536f087a70ab6`  
		Last Modified: Mon, 16 Mar 2026 23:11:18 GMT  
		Size: 1.3 MB (1279856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1077cd177b7cad3d602a07fde8cfb1f7120cb3d374652b67b2366626493cc94`  
		Last Modified: Mon, 16 Mar 2026 23:11:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4661a3095708f309a1743a3b2d5b4c6ac368359732bef7c2b1dec88ad89c00`  
		Last Modified: Mon, 16 Mar 2026 23:11:19 GMT  
		Size: 42.1 MB (42127076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717106f0bff9cfbf1d8c00ef815c4c5644de7a6e65a46c00a7a94d924ae3e479`  
		Last Modified: Mon, 16 Mar 2026 23:11:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05e21871ed88ca83f56952ef1fff9d6eae302d6ef21e25a04a4145732b392a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 6.1 MB (6054358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d693447378ecf8530f5e5ba4e573500973fa2ee25516f6f4c73493cff4c3a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36446a00b3dd3da4571ffd45080ec39040b0d3bfe2b6384527c417b29faad2e`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec69e75e3840dc6f30a1545f3de12b3bfc3653e177637832c36a3daa695cf0`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:fd5f1fdb922c52e7441ec9e197b3e3ade0d70dcbc15012914df9ca92b6ddbbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7490c1bacb57a4d23fa352fa126c44d28cfabb22fdc816b91b969a2edf28af9`

```dockerfile
```

-	Layers:
	-	`sha256:c324c52a2dd211e3dbe7b3a0ab4e53c4ba96377933843df7d1ed8da25fcab571`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33716a313882e7d53c0379971fd6063af2a9a08610bb4fec0845c7790dba0845`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f5e43113eaff653443d9485af541c538a37caf9500ddf2aea7ecdff67b09d32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73090231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21a8f68ce47cc615e162058a6ab896f49fcf0e82f8c9b1a04c94b5c146222a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:11:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:11:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:11:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:11:32 GMT
USER fluent
# Tue, 17 Mar 2026 01:11:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a43a05dbd3979d6f19a9eed8b3d0de971bfa48c3c53ec47d51d7b7bcb4651`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 1.3 MB (1263649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2e8340c868a18a42e59181f9d8524b24ea1dd6b85c2346ebbb407a777f0e2`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211628c31f1b196dd05de247142455ec46f19c2d0ae99be78daa53a1747f6b`  
		Last Modified: Mon, 16 Mar 2026 23:58:18 GMT  
		Size: 37.9 MB (37924120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b448d13fe704838615d979910c81e7aac357cc4dd21d7b73c4eda848c831b4`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9df04d3708ea4652201bd273e80ef0f6bfc99b6cc8462408fd0d0f5685495`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 6.0 MB (5956422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecae936460d331b4b75c996142043e42d708f3b1727e95470be7b050484f14`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13bd6b48910a2334b4b39b4cf38436333a627cf5e97e0bf0eac04769d22d5c5`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9953dd207b1750464e34f6ce106f085dd575c11dcb516b760b35fc889e938`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:587bf90da8db01a6f693c9e4d84096fa64788256ab664fa7f4ec715b74c87f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d7f001f823796cf988502e5dc9b8f1f3a425e12e51fa190711ff0dede0d51`

```dockerfile
```

-	Layers:
	-	`sha256:3eda4bfebd5a8a76c7f826675bd8b9e15729e7c87f6e528d7fd73f1723b0e7c8`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 2.3 MB (2284609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f01bb55871f9b063961672fcbba60c4e6b681e0e05784b2a619a05b266c17`  
		Last Modified: Tue, 17 Mar 2026 01:11:39 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5b1bb23084eef05385f4c4c74e3dd217d75777e06b82de8ad1b84ed3c07f6ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70954354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e1959aa1bb568fdba0c4711afeb0c4dcb57728ac7e5779b5de863c25d08ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:25:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:25:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:25:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:25:40 GMT
USER fluent
# Tue, 17 Mar 2026 01:25:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ce6cc2439c6b79c819ca9430e1bbb77c736ef2b35e42dd774e1ee18b76c924`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 1.2 MB (1237537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633f1380a4453313dbff0278ff9100b83a12c56bf46f93e6494d415adbf7156`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cdbd0c158a2b9bd3c2df11b9e6cbf24979873dcd4dc4f7ff1469aeb58e6cb`  
		Last Modified: Tue, 17 Mar 2026 00:29:18 GMT  
		Size: 37.8 MB (37780498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04683c59e4f85944be0b6ed9bd3f353decd8f53f54f32626c3936940fb9c16`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63790ca04810e0d66155f2f69b901211088284f5ac845b184cf0436e2c15f75`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 5.7 MB (5724425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa89e0a796adaa73e197d3004bd942194ca738139b01e37893e97c60bea10bd`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf7a0fc49c141a5d864b78aded16530a02f8b90eeb110e6a6560e4c68a8424`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e1c7b0665d871ae781d1de8b0072f804c50191b37acfd04efa02b8106960d`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:c24a3a532f92707c6a93e6e8ca3e25c0cc1d5b674a6a71c4d04ae287fcb67f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52aba213be0f8322386168f1d2ec5f581cd3d9cace59f56cd117831b8aeb2911`

```dockerfile
```

-	Layers:
	-	`sha256:e832b0fade97830c666a9062f5a5907fc3c49b3b6623ccd210f8613aa92efc80`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 2.3 MB (2283050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f5bd3f3f0b9cab1b32cd827b01deeb8f18e2df01771c8634c82e9af4240afc`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7657694a7efdd9352062ca5978158d337bb1beff0e26592f6c8d9fa5ec2cfb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715de10dcb59a132e73255d71523d3a62f07f62af4100bdf83588d080a140936`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:28:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:28:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:28:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:28:13 GMT
USER fluent
# Tue, 17 Mar 2026 00:28:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:28:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92a159e78842706770d91322db2570dafe843687416a63a00f853632c63ea2`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 1.3 MB (1261719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bac3edea6f061f16806a6288d6e41577357f3b7b93e488a21e4a7fd4c0026`  
		Last Modified: Mon, 16 Mar 2026 23:16:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f3c5800da728b1d929316f1d9e7922cfd33a0e3837fe5894d84932d7b4bdb`  
		Last Modified: Mon, 16 Mar 2026 23:16:48 GMT  
		Size: 42.1 MB (42078629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f9cb2f0ffe8093241a96360434e49097b4e44d4920a83e5f8bdf651cb44d`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a14dcd72029447494a817832a7e07d7f37242f0dfc61fb95b94f9fd10ca15fe`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57138ce9a8b70f6c7a5d55a09bb75248aaec17efed7f25ade014241a289f6e`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf3ff271f286cbf184eba1d029d53f7e4d984c2f0fb7fd76a8a32cf87250fbc`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3052e2c628efed1916df587fc830bf2a5528dfc750a5bb474c8223c13e81ce`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:c1e88a6ffa3097dc994d4e0991f7f47de295a837f1d4bf29cd561d95217f2be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c90d852e68a0d015595cbf540c9cae739255d59a789697fc41e328e2490548`

```dockerfile
```

-	Layers:
	-	`sha256:e7e9da00a2453346696d204f42c7112fce2e797a2b2a1b6654bfd3835d93a055`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 2.3 MB (2281910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf140398761f442be58afa79e717b45c4944cd5882049553aec402bda080eef1`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:c7d152b9229f3e070984e71e98c800db8e62995055254dcb3f735e3ef991ca17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76267475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2968d7815532be0e8410a27f1cf32e97d4f8af5d651e085d2f00ebe44644d82e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
CMD ["irb"]
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Mon, 16 Mar 2026 23:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 16 Mar 2026 23:58:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 16 Mar 2026 23:58:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 16 Mar 2026 23:58:39 GMT
USER fluent
# Mon, 16 Mar 2026 23:58:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 16 Mar 2026 23:58:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1da629cb883a06ff6b9ef25550345b4927b8b12f06fcbb138f2885887d1e03`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74c8124443e3a5d4ab3af6ec3c78c41fb6dbb305c9a75c723f91fb75b29a05`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab22c27d7d7daa338ddbae9eb6a91201dbaa87d3c9b68dfc028ad3827b4926`  
		Last Modified: Mon, 16 Mar 2026 23:09:48 GMT  
		Size: 37.7 MB (37660763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1abe2b804f27172a8dd698ff935138d6bf544d4bb4d5afe153b1cbab9a717`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4290f2b095cb17fa5d8f2928b201825b76a29726b003cd7b4d09ffaced3b1444`  
		Last Modified: Mon, 16 Mar 2026 23:58:47 GMT  
		Size: 6.0 MB (6025707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78becfe8530cd7d67f676ce149fec997d8bf0d1f12b5d84bbc78a82e5ce3088`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa13de4eb79e4748482048b2895633cd042c017b616f10bce785fbbd27921d56`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7f1df1b6474ed8750845743a45310fb4159c462d804c40a1dcfe3e04311bf`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:def4033cd1eb61c8f859e1fa1e99dd6b751a9a39975446bc009125d847856181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854c24027309a88546e818319a93806640f983b3ffa467e56c3ffed9b62ab973`

```dockerfile
```

-	Layers:
	-	`sha256:74ff77a8b1c990b237ac684de08321e9a1f26ca3191fa09144fb154662e3fce6`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 2.3 MB (2278826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06259fe209d39ca97315e79085c0e75719b4d6374d6481eee7a39e81f5d6d97a`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
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
$ docker pull fluentd@sha256:eea29c28ffa870cf2b759da9107723177e1872a7b4bb808acdd5824a14da0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76768794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7626f6e598ea93ab08fe91ea8e27b673ce3a92ce423257ab8469a1b9afec1ec1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 02:48:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 02:48:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 02:48:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 02:48:57 GMT
USER fluent
# Tue, 17 Mar 2026 02:48:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 02:48:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4fe3d99fd095b557f25c59245ba2eddb03ddc5040b30df042c597414c5f212`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 1.3 MB (1294694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128cee34993f6c191f293eb8726195324ee885bed43e321dae78c2d5a587fb8`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef60ac4e1282f8d5263cfd4dfb9c79a81dea7281fbb918a416e612c6d2598873`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 39.2 MB (39205981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992f744f5644cd6eaa8857bb9dbe0183992f21edf8be831e65a0d6a43d53eed`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e996c0ec018487718aa8c8b4101d230fde49e4b2f64e7b3b49ecae7e187c07`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 6.4 MB (6430464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ff921c60727ad35dc3d3e4e3ca80447343da2d0ee4e1d8460f1bf2409a190`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64b7573dd7428082c55d68ce5af8c9259740d0e341a3c2aec87acd86d6df32`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1222d11abbb4ea3cfb093b455e5588ce03875fa1cfb6113c4ec0c5a1cbac763c`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:3882951f6afb4f316675d42e8a3e4b8dd88c05a8a754c9dcb3d64a12a066a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60aff89ba5a2e93bd4208b4befe75569964b442975cb9fc834639eee1177c1`

```dockerfile
```

-	Layers:
	-	`sha256:b4cf9b5f9b538b89a773bdcbfa035284cac0929226815dea238f80484048e28b`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 2.3 MB (2283083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e921159af6f57b2331258fbbe8e7b9da4f51b4f13b9d6cf2be40decdeed8c0a`  
		Last Modified: Tue, 17 Mar 2026 02:49:15 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:a4aca9d4d6e742f9c449901b07c4c1820e40d700f8f40849df80f08a41fb99c5
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
$ docker pull fluentd@sha256:4fada955f0cc16c6f59b36a15be17cae191b5d14cf82636113607efffcd30544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81808199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cceff91d6665cbed499cbec20aceb5678a15b97e36cbaa4b1759715b8a08fdd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:14:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:14:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:14:23 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:14:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:14:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:14:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:14:23 GMT
USER fluent
# Fri, 27 Mar 2026 19:14:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720da4786f774f8d50db8269e399bff3b9e1bbe5e88660c364c3726d3d0e661`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 3.5 MB (3510177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d642b6c07a15b274745714c90ba586bbda858c0743c424e25c4fe65f9e72638`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0de75d88464c3b86f05c31ec678872cfc37965c2310aaeb0341661c22d8b40`  
		Last Modified: Fri, 27 Mar 2026 18:33:04 GMT  
		Size: 35.8 MB (35781138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a46dbbfef6573a04e2100855782d74436470062933cd957ff448cd366aa16c`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d72dde64a856f017e64f69e07d6d1d89bd15552655aaa8bc5ec2fb79ec1c529`  
		Last Modified: Fri, 27 Mar 2026 19:14:33 GMT  
		Size: 14.3 MB (14278266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94645ac647d25e07d9430b5db0ac5d7e437629331db28bd1787df53ab233d25e`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eb456f0027e96f36cfe1b32a6eeb5824725454284f42a368a4867d11cdf29b`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceefa8787b03579869004ba8ca72b29d8ad24e1fbf8a98056523e1a7560b086b`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cfba8e282829240b8558e20ba225b0fbe045bda6ab7a5ca5a6baf8fafb00480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d58d166fc688f33d576120ee4e7433ecc90dc690a99cd3bbb0a7a795b6ba2b1`

```dockerfile
```

-	Layers:
	-	`sha256:be0101331bc514c5697e330c85a841dcc8d30c2a04ae05b8c9518ffe2f0a8bad`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:847dc6074771752d5981963d1905e572afc47e8e5e841d20a4a5a955861d4290`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:1ab2431189127bed38b93b5b553af981a16853e7fb1afcf57842b44b49f457c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75192766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e60f2f70e506ad1d9c94d9d8b4bdd48be910d4cc5f4bcedadfa9e05a9119884`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:31:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:33:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:33:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:16:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:16:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:16:00 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:16:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:16:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:16:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:16:00 GMT
USER fluent
# Fri, 27 Mar 2026 19:16:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:16:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0509921ab3afd77666b790895956e135e1e2fb4d8f883e8875dc39cf1523d`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 3.1 MB (3081057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acab53a82fd491be855c7b0fc4a36c627f104b6c3263bef951fe827b8d4ca6f`  
		Last Modified: Fri, 27 Mar 2026 18:33:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c621ddf033909815378f5cc2169fac84a35fbc3f726e689ee8350fe4223a284`  
		Last Modified: Fri, 27 Mar 2026 18:33:57 GMT  
		Size: 32.1 MB (32078792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5592a792a05e3913768ff79d875f8b92fc9d6e060001a5f4cfb79378dc86ae5`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6eb44834f3364f6017937d6ea0dbfea4b9100664591707407ee0a5168b2083a`  
		Last Modified: Fri, 27 Mar 2026 19:16:09 GMT  
		Size: 14.3 MB (14264915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6fa4e01e371b60bc01cc7697ad165716947b6ba04d8cdd9175edd7d30be50e`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d3709e3b008f5017c868f9f2e47d1de6b19566e00ed70f4965a550705f0104`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c22aa997362b396038b3730fae10b86fa0a07f68a2ab414583e353c370bdf51`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:77ab52622ac4beec749b9980a66acb8e1003efcd5e3fbe9b578bc379d0438b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943fdaa12164c45a2a3313c05ca25591f6c9bc6d3a13b869477ef043130965f2`

```dockerfile
```

-	Layers:
	-	`sha256:56c166971229636dd93b713d432d078c0601baa72a5aa0094ff7842afd4ece45`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8033e348db20fbbb28a8ad449fcf88d94301aa6634f1aad4f55597317d545db1`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:8c3b56ec413bec0c6bf6f782e409ed13970ac635ab07e17f1fa5c20123c97222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72950430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9027e7fab3dfafe32ffbf62515d39851db0453415af6d66715839aa8056f26b8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:12:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:12:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:12:38 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:12:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:12:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:12:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:12:38 GMT
USER fluent
# Fri, 27 Mar 2026 19:12:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:12:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f749ab8f1791ed041d0530e13b98c95fcbbb10309364f9870dab9c3ebc63a0e3`  
		Last Modified: Fri, 27 Mar 2026 18:32:19 GMT  
		Size: 2.9 MB (2913749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b85973033435846f63211a0e6d84df6f59c91fee986c4cfe8e6afda18fb45`  
		Last Modified: Fri, 27 Mar 2026 18:32:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22859a0ef0349e1365deaef26124871c19d64ec4ab2a695b01ae8d4e82647e`  
		Last Modified: Fri, 27 Mar 2026 18:32:20 GMT  
		Size: 31.9 MB (31909950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080355c19138d7ca4214a6834881f793e5de716b880a70ba0ca8be3fa48358da`  
		Last Modified: Fri, 27 Mar 2026 18:32:19 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a560b5317154622eb2a6cc847fd6339fd6759ab40a3f549ade721e59674227a`  
		Last Modified: Fri, 27 Mar 2026 19:12:47 GMT  
		Size: 14.2 MB (14182991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b21af0e88c3a6ab54258c64c5b94969d571e097bf61a6f61771b8fac9e787c1`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a430c303dddf8cd38f1743fc40fe3bbefe5e3be73d15dd8940499610c7c40c`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa967ab388d266115b529629d68eda6ee5e07c80d004e07c57195c4e0efbbde`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:849e6976e9a45e369673e7c36f2d49905672bbf74dc44fa9abb19fa7c93cc4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a648ac05aa0eb89b12e308247dc6b493ea05cea4626997464ac0716b5cd9b64`

```dockerfile
```

-	Layers:
	-	`sha256:37e88ef6dcf5c8a088a8d088798a997b5b368981faffd3eebc8c82546574a99f`  
		Last Modified: Fri, 27 Mar 2026 19:12:47 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c992568b26776f61317274ac9144416efd3543dc3949f7e1861d469d00f1674a`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:11186824d095331bb878aa3417f2dc9deb611565585acfee082e9a3174ffcfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81425488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece4aa105ab31d3ab22584da8540399c5208e474814225d90780c3efc938639`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:14:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:14:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:14:47 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:14:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:14:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:14:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:14:47 GMT
USER fluent
# Fri, 27 Mar 2026 19:14:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2bf29c161d4b803874a4a08b0e4cc7ddfbeb28ff4cb0f9250fa2091aec487`  
		Last Modified: Fri, 27 Mar 2026 18:32:30 GMT  
		Size: 3.3 MB (3341466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f3635f949b1ab6e024c4f0132bebcc74ef2c37d7f9f15fa2104d9c02701c8f`  
		Last Modified: Fri, 27 Mar 2026 18:32:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e98fb07534e2ab6d3659470de49ced2eb1db0d89cf522434f91e39a71e75295`  
		Last Modified: Fri, 27 Mar 2026 18:32:32 GMT  
		Size: 35.7 MB (35687892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228cb8d5c23dc24db4673bb1850afd347fb1f213ba80fbb685958d8c3c7c891`  
		Last Modified: Fri, 27 Mar 2026 18:32:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad62e019aa5b766c4b83f2fbbf66eb42536d105511de2dbd1a4cdfce5531aa3`  
		Last Modified: Fri, 27 Mar 2026 19:14:57 GMT  
		Size: 14.3 MB (14277669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e02d519e80cb119d44817cde8ac3f04a8c5c890da0abf53355a7d5f5af7de00`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0524e02024ba1d1a434a2062a5ba6a905ce177301ffc55bfc0d6f4f3afa8c3c`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0383888cd81153de4e16bfc284d3771cb6fbaeb39f72277c1844fa3210321519`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:499e8bae9c4266d42dac17fbd4bd963a8d58a37d33b6bdfdc7b85ba8ebe1df33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2d38d3aeda16a16db8069e4f6707fe6de970eede4e9734956a1bf412321fa5`

```dockerfile
```

-	Layers:
	-	`sha256:0cc6fcf876a0ea277bae63ae5b5200a98f1c8f8d17aac59ea37e2e3e48211b47`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d68b6261e2384898b98ff42b17190879bbcc91a0dcaef1e2433eb62800dfb0`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5e1f7d80b21c1d6e33b8c569953a11b9a0ba9dfb845017ebacf3d70a0347c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78687539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de39bdac86010188dc67c91f47ea8c507fb9f8a9c178a34c499ffb63718a4566`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:13:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:13:17 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:13:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:13:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:13:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:13:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:13:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:13:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:13:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:13:18 GMT
USER fluent
# Fri, 27 Mar 2026 19:13:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:13:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be82ffbcf8ae3cdc7b1e40d90551ea955c0ea03e9e844610ffc274b66f9e82`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 3.5 MB (3512915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef216bd1074e05ab1fb22dff507b71b91d11763ca49bd7be4c5958e1d0f753c`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9630165582738c6fc95fba61bcebb6724044d6f804aa3010c1c1fef82f9147`  
		Last Modified: Fri, 27 Mar 2026 18:32:42 GMT  
		Size: 31.9 MB (31884076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12128aab6ee45e8777710bbe7a6f5f738c643fadacf4178a7d4445a4891aa9e3`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011b928e27bd1b4384fcc5952f264b1b9780bb01c414055d7c330453ab335473`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 14.1 MB (14066473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0f6d28eeafac90cdfae106098ef3816e369b18a52ef3771a7a09fb1b1dcc8`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dac50f41ef97e532cc47f9705142d62cfc00f89ad824792a7d4da714955065`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f467bcc2abe8e816f7246823af2f258f1a84bdcbdf13c262f32fa55af6104`  
		Last Modified: Fri, 27 Mar 2026 19:13:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:97b07eeaf91aacf3d10b37b89e8d3fd86daf9a6afec4ebb882fa020e79f8f953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b599eedd08525747f7d89b293c1f24a3ee6bde2a537fdca5588c1cafcb430a`

```dockerfile
```

-	Layers:
	-	`sha256:e1dd3cfa8deaf3a2d6aec636185b4bf56898689346eeb6393876818dbb47bfef`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22cfb068c0685856f8649b151b32b3022505eba6e88b4546b52baf194ce3209a`  
		Last Modified: Fri, 27 Mar 2026 19:13:25 GMT  
		Size: 21.0 KB (21046 bytes)  
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
$ docker pull fluentd@sha256:5feadfd8efd23d81a5603940252e04db26d13fd6e675d98dbe2e5d2c64caff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77346247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245ec335070e32ef4ab9e506a0af6d3def5b478bdf9dcd127c140cf7dc77250`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:28:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:31:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:31:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:31:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:31:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:13:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:13:14 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:13:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:13:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:13:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:13:14 GMT
USER fluent
# Fri, 27 Mar 2026 19:13:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:13:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa423bc82dbe9900983364c79e98ab227be4db425af41a7c5ddf086cb1442cba`  
		Last Modified: Thu, 26 Mar 2026 18:29:16 GMT  
		Size: 3.2 MB (3171221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04c640b78ba55a660ffb68f109902ea1388e342f84298445d0a8e9b778ab6ec`  
		Last Modified: Fri, 27 Mar 2026 18:31:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d06d395c0114f0c458dbb46affdaca647bac522090cf8b13de69cd9e6c6bda`  
		Last Modified: Fri, 27 Mar 2026 18:31:28 GMT  
		Size: 32.9 MB (32875224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ca8834f25ee1e990c6f4f11d81385b6db6388d3c3777a86d6e447acee6a75`  
		Last Modified: Fri, 27 Mar 2026 18:31:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276976570ca9804582e0d60153ccda97bd03a582a34182e7aad68dd3b5a70e8d`  
		Last Modified: Fri, 27 Mar 2026 19:13:28 GMT  
		Size: 14.4 MB (14405893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4c72c44e028e456eeb0db3db1c64bf9a95c6797896aa032f72bdfc0abee6a0`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870ea32a65d3ee1b157cf09afee7fae83c919d62c106058ee6b750ae103dcfcf`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ecba8e15ccf8475186b85609468af04027a34e138d66b47c81c95cc4b8675`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3e0374d2b2d18012433665d0386de757128fa3232628a2a60f36ffb81edd2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff6fee12935279815b7bc77c2438bc128db6f6a2b79bc618c0283d9a96e0bf9`

```dockerfile
```

-	Layers:
	-	`sha256:bc959fd5ac9f1fe09784ad486a6a9a5dadc81a5f8dd11b058b1c219d3833667e`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80dcabba48c2c53584397e23429cd1e928b4d84c2a2e6c6a8d434c1a487b4af0`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:a4aca9d4d6e742f9c449901b07c4c1820e40d700f8f40849df80f08a41fb99c5
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
$ docker pull fluentd@sha256:4fada955f0cc16c6f59b36a15be17cae191b5d14cf82636113607efffcd30544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81808199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cceff91d6665cbed499cbec20aceb5678a15b97e36cbaa4b1759715b8a08fdd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:14:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:14:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:14:23 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:14:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:14:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:14:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:14:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:14:23 GMT
USER fluent
# Fri, 27 Mar 2026 19:14:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720da4786f774f8d50db8269e399bff3b9e1bbe5e88660c364c3726d3d0e661`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 3.5 MB (3510177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d642b6c07a15b274745714c90ba586bbda858c0743c424e25c4fe65f9e72638`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0de75d88464c3b86f05c31ec678872cfc37965c2310aaeb0341661c22d8b40`  
		Last Modified: Fri, 27 Mar 2026 18:33:04 GMT  
		Size: 35.8 MB (35781138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a46dbbfef6573a04e2100855782d74436470062933cd957ff448cd366aa16c`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d72dde64a856f017e64f69e07d6d1d89bd15552655aaa8bc5ec2fb79ec1c529`  
		Last Modified: Fri, 27 Mar 2026 19:14:33 GMT  
		Size: 14.3 MB (14278266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94645ac647d25e07d9430b5db0ac5d7e437629331db28bd1787df53ab233d25e`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eb456f0027e96f36cfe1b32a6eeb5824725454284f42a368a4867d11cdf29b`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceefa8787b03579869004ba8ca72b29d8ad24e1fbf8a98056523e1a7560b086b`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cfba8e282829240b8558e20ba225b0fbe045bda6ab7a5ca5a6baf8fafb00480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d58d166fc688f33d576120ee4e7433ecc90dc690a99cd3bbb0a7a795b6ba2b1`

```dockerfile
```

-	Layers:
	-	`sha256:be0101331bc514c5697e330c85a841dcc8d30c2a04ae05b8c9518ffe2f0a8bad`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:847dc6074771752d5981963d1905e572afc47e8e5e841d20a4a5a955861d4290`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:1ab2431189127bed38b93b5b553af981a16853e7fb1afcf57842b44b49f457c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75192766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e60f2f70e506ad1d9c94d9d8b4bdd48be910d4cc5f4bcedadfa9e05a9119884`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:31:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:33:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:33:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:16:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:16:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:16:00 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:16:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:16:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:16:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:16:00 GMT
USER fluent
# Fri, 27 Mar 2026 19:16:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:16:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0509921ab3afd77666b790895956e135e1e2fb4d8f883e8875dc39cf1523d`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 3.1 MB (3081057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acab53a82fd491be855c7b0fc4a36c627f104b6c3263bef951fe827b8d4ca6f`  
		Last Modified: Fri, 27 Mar 2026 18:33:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c621ddf033909815378f5cc2169fac84a35fbc3f726e689ee8350fe4223a284`  
		Last Modified: Fri, 27 Mar 2026 18:33:57 GMT  
		Size: 32.1 MB (32078792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5592a792a05e3913768ff79d875f8b92fc9d6e060001a5f4cfb79378dc86ae5`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6eb44834f3364f6017937d6ea0dbfea4b9100664591707407ee0a5168b2083a`  
		Last Modified: Fri, 27 Mar 2026 19:16:09 GMT  
		Size: 14.3 MB (14264915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6fa4e01e371b60bc01cc7697ad165716947b6ba04d8cdd9175edd7d30be50e`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d3709e3b008f5017c868f9f2e47d1de6b19566e00ed70f4965a550705f0104`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c22aa997362b396038b3730fae10b86fa0a07f68a2ab414583e353c370bdf51`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:77ab52622ac4beec749b9980a66acb8e1003efcd5e3fbe9b578bc379d0438b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943fdaa12164c45a2a3313c05ca25591f6c9bc6d3a13b869477ef043130965f2`

```dockerfile
```

-	Layers:
	-	`sha256:56c166971229636dd93b713d432d078c0601baa72a5aa0094ff7842afd4ece45`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8033e348db20fbbb28a8ad449fcf88d94301aa6634f1aad4f55597317d545db1`  
		Last Modified: Fri, 27 Mar 2026 19:16:08 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:8c3b56ec413bec0c6bf6f782e409ed13970ac635ab07e17f1fa5c20123c97222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72950430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9027e7fab3dfafe32ffbf62515d39851db0453415af6d66715839aa8056f26b8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:12:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:12:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:12:38 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:12:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:12:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:12:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:12:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:12:38 GMT
USER fluent
# Fri, 27 Mar 2026 19:12:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:12:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f749ab8f1791ed041d0530e13b98c95fcbbb10309364f9870dab9c3ebc63a0e3`  
		Last Modified: Fri, 27 Mar 2026 18:32:19 GMT  
		Size: 2.9 MB (2913749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b85973033435846f63211a0e6d84df6f59c91fee986c4cfe8e6afda18fb45`  
		Last Modified: Fri, 27 Mar 2026 18:32:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22859a0ef0349e1365deaef26124871c19d64ec4ab2a695b01ae8d4e82647e`  
		Last Modified: Fri, 27 Mar 2026 18:32:20 GMT  
		Size: 31.9 MB (31909950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080355c19138d7ca4214a6834881f793e5de716b880a70ba0ca8be3fa48358da`  
		Last Modified: Fri, 27 Mar 2026 18:32:19 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a560b5317154622eb2a6cc847fd6339fd6759ab40a3f549ade721e59674227a`  
		Last Modified: Fri, 27 Mar 2026 19:12:47 GMT  
		Size: 14.2 MB (14182991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b21af0e88c3a6ab54258c64c5b94969d571e097bf61a6f61771b8fac9e787c1`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a430c303dddf8cd38f1743fc40fe3bbefe5e3be73d15dd8940499610c7c40c`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa967ab388d266115b529629d68eda6ee5e07c80d004e07c57195c4e0efbbde`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:849e6976e9a45e369673e7c36f2d49905672bbf74dc44fa9abb19fa7c93cc4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a648ac05aa0eb89b12e308247dc6b493ea05cea4626997464ac0716b5cd9b64`

```dockerfile
```

-	Layers:
	-	`sha256:37e88ef6dcf5c8a088a8d088798a997b5b368981faffd3eebc8c82546574a99f`  
		Last Modified: Fri, 27 Mar 2026 19:12:47 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c992568b26776f61317274ac9144416efd3543dc3949f7e1861d469d00f1674a`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:11186824d095331bb878aa3417f2dc9deb611565585acfee082e9a3174ffcfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81425488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece4aa105ab31d3ab22584da8540399c5208e474814225d90780c3efc938639`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:14:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:14:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:14:47 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:14:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:14:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:14:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:14:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:14:47 GMT
USER fluent
# Fri, 27 Mar 2026 19:14:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2bf29c161d4b803874a4a08b0e4cc7ddfbeb28ff4cb0f9250fa2091aec487`  
		Last Modified: Fri, 27 Mar 2026 18:32:30 GMT  
		Size: 3.3 MB (3341466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f3635f949b1ab6e024c4f0132bebcc74ef2c37d7f9f15fa2104d9c02701c8f`  
		Last Modified: Fri, 27 Mar 2026 18:32:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e98fb07534e2ab6d3659470de49ced2eb1db0d89cf522434f91e39a71e75295`  
		Last Modified: Fri, 27 Mar 2026 18:32:32 GMT  
		Size: 35.7 MB (35687892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228cb8d5c23dc24db4673bb1850afd347fb1f213ba80fbb685958d8c3c7c891`  
		Last Modified: Fri, 27 Mar 2026 18:32:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad62e019aa5b766c4b83f2fbbf66eb42536d105511de2dbd1a4cdfce5531aa3`  
		Last Modified: Fri, 27 Mar 2026 19:14:57 GMT  
		Size: 14.3 MB (14277669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e02d519e80cb119d44817cde8ac3f04a8c5c890da0abf53355a7d5f5af7de00`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0524e02024ba1d1a434a2062a5ba6a905ce177301ffc55bfc0d6f4f3afa8c3c`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0383888cd81153de4e16bfc284d3771cb6fbaeb39f72277c1844fa3210321519`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:499e8bae9c4266d42dac17fbd4bd963a8d58a37d33b6bdfdc7b85ba8ebe1df33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2d38d3aeda16a16db8069e4f6707fe6de970eede4e9734956a1bf412321fa5`

```dockerfile
```

-	Layers:
	-	`sha256:0cc6fcf876a0ea277bae63ae5b5200a98f1c8f8d17aac59ea37e2e3e48211b47`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d68b6261e2384898b98ff42b17190879bbcc91a0dcaef1e2433eb62800dfb0`  
		Last Modified: Fri, 27 Mar 2026 19:14:56 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5e1f7d80b21c1d6e33b8c569953a11b9a0ba9dfb845017ebacf3d70a0347c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78687539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de39bdac86010188dc67c91f47ea8c507fb9f8a9c178a34c499ffb63718a4566`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:13:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:13:17 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:13:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:13:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:13:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:13:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:13:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:13:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:13:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:13:18 GMT
USER fluent
# Fri, 27 Mar 2026 19:13:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:13:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be82ffbcf8ae3cdc7b1e40d90551ea955c0ea03e9e844610ffc274b66f9e82`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 3.5 MB (3512915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef216bd1074e05ab1fb22dff507b71b91d11763ca49bd7be4c5958e1d0f753c`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9630165582738c6fc95fba61bcebb6724044d6f804aa3010c1c1fef82f9147`  
		Last Modified: Fri, 27 Mar 2026 18:32:42 GMT  
		Size: 31.9 MB (31884076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12128aab6ee45e8777710bbe7a6f5f738c643fadacf4178a7d4445a4891aa9e3`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011b928e27bd1b4384fcc5952f264b1b9780bb01c414055d7c330453ab335473`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 14.1 MB (14066473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0f6d28eeafac90cdfae106098ef3816e369b18a52ef3771a7a09fb1b1dcc8`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dac50f41ef97e532cc47f9705142d62cfc00f89ad824792a7d4da714955065`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f467bcc2abe8e816f7246823af2f258f1a84bdcbdf13c262f32fa55af6104`  
		Last Modified: Fri, 27 Mar 2026 19:13:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:97b07eeaf91aacf3d10b37b89e8d3fd86daf9a6afec4ebb882fa020e79f8f953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b599eedd08525747f7d89b293c1f24a3ee6bde2a537fdca5588c1cafcb430a`

```dockerfile
```

-	Layers:
	-	`sha256:e1dd3cfa8deaf3a2d6aec636185b4bf56898689346eeb6393876818dbb47bfef`  
		Last Modified: Fri, 27 Mar 2026 19:13:26 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22cfb068c0685856f8649b151b32b3022505eba6e88b4546b52baf194ce3209a`  
		Last Modified: Fri, 27 Mar 2026 19:13:25 GMT  
		Size: 21.0 KB (21046 bytes)  
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
$ docker pull fluentd@sha256:5feadfd8efd23d81a5603940252e04db26d13fd6e675d98dbe2e5d2c64caff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77346247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245ec335070e32ef4ab9e506a0af6d3def5b478bdf9dcd127c140cf7dc77250`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:28:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:31:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:31:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:31:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:31:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:13:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:13:14 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:13:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:13:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:13:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:13:14 GMT
USER fluent
# Fri, 27 Mar 2026 19:13:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:13:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa423bc82dbe9900983364c79e98ab227be4db425af41a7c5ddf086cb1442cba`  
		Last Modified: Thu, 26 Mar 2026 18:29:16 GMT  
		Size: 3.2 MB (3171221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04c640b78ba55a660ffb68f109902ea1388e342f84298445d0a8e9b778ab6ec`  
		Last Modified: Fri, 27 Mar 2026 18:31:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d06d395c0114f0c458dbb46affdaca647bac522090cf8b13de69cd9e6c6bda`  
		Last Modified: Fri, 27 Mar 2026 18:31:28 GMT  
		Size: 32.9 MB (32875224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ca8834f25ee1e990c6f4f11d81385b6db6388d3c3777a86d6e447acee6a75`  
		Last Modified: Fri, 27 Mar 2026 18:31:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276976570ca9804582e0d60153ccda97bd03a582a34182e7aad68dd3b5a70e8d`  
		Last Modified: Fri, 27 Mar 2026 19:13:28 GMT  
		Size: 14.4 MB (14405893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4c72c44e028e456eeb0db3db1c64bf9a95c6797896aa032f72bdfc0abee6a0`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870ea32a65d3ee1b157cf09afee7fae83c919d62c106058ee6b750ae103dcfcf`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ecba8e15ccf8475186b85609468af04027a34e138d66b47c81c95cc4b8675`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3e0374d2b2d18012433665d0386de757128fa3232628a2a60f36ffb81edd2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff6fee12935279815b7bc77c2438bc128db6f6a2b79bc618c0283d9a96e0bf9`

```dockerfile
```

-	Layers:
	-	`sha256:bc959fd5ac9f1fe09784ad486a6a9a5dadc81a5f8dd11b058b1c219d3833667e`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80dcabba48c2c53584397e23429cd1e928b4d84c2a2e6c6a8d434c1a487b4af0`  
		Last Modified: Fri, 27 Mar 2026 19:13:27 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:b48a22c6359bd460092ae16029c2367e65298eb946f9f0d6731aa8c168185fd1
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
$ docker pull fluentd@sha256:232406cf7372ec3334cc854604c6e4da073278562f45b4f4ba1999c1b0bdcb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79239187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160b4477cbc5df32a10ae2e9d2c1d4ace19b5e42149b80e2f51aebd182a1e0c8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:27:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:27:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:27:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:27:58 GMT
USER fluent
# Tue, 17 Mar 2026 00:27:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:27:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c59864e0006c1e4962cbce8eefb3283a4a8eb888aab9f56e43536f087a70ab6`  
		Last Modified: Mon, 16 Mar 2026 23:11:18 GMT  
		Size: 1.3 MB (1279856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1077cd177b7cad3d602a07fde8cfb1f7120cb3d374652b67b2366626493cc94`  
		Last Modified: Mon, 16 Mar 2026 23:11:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4661a3095708f309a1743a3b2d5b4c6ac368359732bef7c2b1dec88ad89c00`  
		Last Modified: Mon, 16 Mar 2026 23:11:19 GMT  
		Size: 42.1 MB (42127076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717106f0bff9cfbf1d8c00ef815c4c5644de7a6e65a46c00a7a94d924ae3e479`  
		Last Modified: Mon, 16 Mar 2026 23:11:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05e21871ed88ca83f56952ef1fff9d6eae302d6ef21e25a04a4145732b392a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 6.1 MB (6054358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d693447378ecf8530f5e5ba4e573500973fa2ee25516f6f4c73493cff4c3a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36446a00b3dd3da4571ffd45080ec39040b0d3bfe2b6384527c417b29faad2e`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec69e75e3840dc6f30a1545f3de12b3bfc3653e177637832c36a3daa695cf0`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fd5f1fdb922c52e7441ec9e197b3e3ade0d70dcbc15012914df9ca92b6ddbbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7490c1bacb57a4d23fa352fa126c44d28cfabb22fdc816b91b969a2edf28af9`

```dockerfile
```

-	Layers:
	-	`sha256:c324c52a2dd211e3dbe7b3a0ab4e53c4ba96377933843df7d1ed8da25fcab571`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33716a313882e7d53c0379971fd6063af2a9a08610bb4fec0845c7790dba0845`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f5e43113eaff653443d9485af541c538a37caf9500ddf2aea7ecdff67b09d32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73090231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21a8f68ce47cc615e162058a6ab896f49fcf0e82f8c9b1a04c94b5c146222a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:11:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:11:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:11:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:11:32 GMT
USER fluent
# Tue, 17 Mar 2026 01:11:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a43a05dbd3979d6f19a9eed8b3d0de971bfa48c3c53ec47d51d7b7bcb4651`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 1.3 MB (1263649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2e8340c868a18a42e59181f9d8524b24ea1dd6b85c2346ebbb407a777f0e2`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211628c31f1b196dd05de247142455ec46f19c2d0ae99be78daa53a1747f6b`  
		Last Modified: Mon, 16 Mar 2026 23:58:18 GMT  
		Size: 37.9 MB (37924120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b448d13fe704838615d979910c81e7aac357cc4dd21d7b73c4eda848c831b4`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9df04d3708ea4652201bd273e80ef0f6bfc99b6cc8462408fd0d0f5685495`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 6.0 MB (5956422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecae936460d331b4b75c996142043e42d708f3b1727e95470be7b050484f14`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13bd6b48910a2334b4b39b4cf38436333a627cf5e97e0bf0eac04769d22d5c5`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9953dd207b1750464e34f6ce106f085dd575c11dcb516b760b35fc889e938`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:587bf90da8db01a6f693c9e4d84096fa64788256ab664fa7f4ec715b74c87f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d7f001f823796cf988502e5dc9b8f1f3a425e12e51fa190711ff0dede0d51`

```dockerfile
```

-	Layers:
	-	`sha256:3eda4bfebd5a8a76c7f826675bd8b9e15729e7c87f6e528d7fd73f1723b0e7c8`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 2.3 MB (2284609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f01bb55871f9b063961672fcbba60c4e6b681e0e05784b2a619a05b266c17`  
		Last Modified: Tue, 17 Mar 2026 01:11:39 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5b1bb23084eef05385f4c4c74e3dd217d75777e06b82de8ad1b84ed3c07f6ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70954354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e1959aa1bb568fdba0c4711afeb0c4dcb57728ac7e5779b5de863c25d08ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:25:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:25:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:25:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:25:40 GMT
USER fluent
# Tue, 17 Mar 2026 01:25:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ce6cc2439c6b79c819ca9430e1bbb77c736ef2b35e42dd774e1ee18b76c924`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 1.2 MB (1237537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633f1380a4453313dbff0278ff9100b83a12c56bf46f93e6494d415adbf7156`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cdbd0c158a2b9bd3c2df11b9e6cbf24979873dcd4dc4f7ff1469aeb58e6cb`  
		Last Modified: Tue, 17 Mar 2026 00:29:18 GMT  
		Size: 37.8 MB (37780498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04683c59e4f85944be0b6ed9bd3f353decd8f53f54f32626c3936940fb9c16`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63790ca04810e0d66155f2f69b901211088284f5ac845b184cf0436e2c15f75`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 5.7 MB (5724425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa89e0a796adaa73e197d3004bd942194ca738139b01e37893e97c60bea10bd`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf7a0fc49c141a5d864b78aded16530a02f8b90eeb110e6a6560e4c68a8424`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e1c7b0665d871ae781d1de8b0072f804c50191b37acfd04efa02b8106960d`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c24a3a532f92707c6a93e6e8ca3e25c0cc1d5b674a6a71c4d04ae287fcb67f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52aba213be0f8322386168f1d2ec5f581cd3d9cace59f56cd117831b8aeb2911`

```dockerfile
```

-	Layers:
	-	`sha256:e832b0fade97830c666a9062f5a5907fc3c49b3b6623ccd210f8613aa92efc80`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 2.3 MB (2283050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f5bd3f3f0b9cab1b32cd827b01deeb8f18e2df01771c8634c82e9af4240afc`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7657694a7efdd9352062ca5978158d337bb1beff0e26592f6c8d9fa5ec2cfb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715de10dcb59a132e73255d71523d3a62f07f62af4100bdf83588d080a140936`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:28:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:28:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:28:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:28:13 GMT
USER fluent
# Tue, 17 Mar 2026 00:28:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:28:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92a159e78842706770d91322db2570dafe843687416a63a00f853632c63ea2`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 1.3 MB (1261719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bac3edea6f061f16806a6288d6e41577357f3b7b93e488a21e4a7fd4c0026`  
		Last Modified: Mon, 16 Mar 2026 23:16:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f3c5800da728b1d929316f1d9e7922cfd33a0e3837fe5894d84932d7b4bdb`  
		Last Modified: Mon, 16 Mar 2026 23:16:48 GMT  
		Size: 42.1 MB (42078629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f9cb2f0ffe8093241a96360434e49097b4e44d4920a83e5f8bdf651cb44d`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a14dcd72029447494a817832a7e07d7f37242f0dfc61fb95b94f9fd10ca15fe`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57138ce9a8b70f6c7a5d55a09bb75248aaec17efed7f25ade014241a289f6e`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf3ff271f286cbf184eba1d029d53f7e4d984c2f0fb7fd76a8a32cf87250fbc`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3052e2c628efed1916df587fc830bf2a5528dfc750a5bb474c8223c13e81ce`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c1e88a6ffa3097dc994d4e0991f7f47de295a837f1d4bf29cd561d95217f2be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c90d852e68a0d015595cbf540c9cae739255d59a789697fc41e328e2490548`

```dockerfile
```

-	Layers:
	-	`sha256:e7e9da00a2453346696d204f42c7112fce2e797a2b2a1b6654bfd3835d93a055`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 2.3 MB (2281910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf140398761f442be58afa79e717b45c4944cd5882049553aec402bda080eef1`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:c7d152b9229f3e070984e71e98c800db8e62995055254dcb3f735e3ef991ca17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76267475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2968d7815532be0e8410a27f1cf32e97d4f8af5d651e085d2f00ebe44644d82e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
CMD ["irb"]
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Mon, 16 Mar 2026 23:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 16 Mar 2026 23:58:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 16 Mar 2026 23:58:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 16 Mar 2026 23:58:39 GMT
USER fluent
# Mon, 16 Mar 2026 23:58:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 16 Mar 2026 23:58:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1da629cb883a06ff6b9ef25550345b4927b8b12f06fcbb138f2885887d1e03`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74c8124443e3a5d4ab3af6ec3c78c41fb6dbb305c9a75c723f91fb75b29a05`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab22c27d7d7daa338ddbae9eb6a91201dbaa87d3c9b68dfc028ad3827b4926`  
		Last Modified: Mon, 16 Mar 2026 23:09:48 GMT  
		Size: 37.7 MB (37660763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1abe2b804f27172a8dd698ff935138d6bf544d4bb4d5afe153b1cbab9a717`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4290f2b095cb17fa5d8f2928b201825b76a29726b003cd7b4d09ffaced3b1444`  
		Last Modified: Mon, 16 Mar 2026 23:58:47 GMT  
		Size: 6.0 MB (6025707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78becfe8530cd7d67f676ce149fec997d8bf0d1f12b5d84bbc78a82e5ce3088`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa13de4eb79e4748482048b2895633cd042c017b616f10bce785fbbd27921d56`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7f1df1b6474ed8750845743a45310fb4159c462d804c40a1dcfe3e04311bf`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:def4033cd1eb61c8f859e1fa1e99dd6b751a9a39975446bc009125d847856181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854c24027309a88546e818319a93806640f983b3ffa467e56c3ffed9b62ab973`

```dockerfile
```

-	Layers:
	-	`sha256:74ff77a8b1c990b237ac684de08321e9a1f26ca3191fa09144fb154662e3fce6`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 2.3 MB (2278826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06259fe209d39ca97315e79085c0e75719b4d6374d6481eee7a39e81f5d6d97a`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
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
$ docker pull fluentd@sha256:eea29c28ffa870cf2b759da9107723177e1872a7b4bb808acdd5824a14da0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76768794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7626f6e598ea93ab08fe91ea8e27b673ce3a92ce423257ab8469a1b9afec1ec1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 02:48:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 02:48:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 02:48:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 02:48:57 GMT
USER fluent
# Tue, 17 Mar 2026 02:48:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 02:48:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4fe3d99fd095b557f25c59245ba2eddb03ddc5040b30df042c597414c5f212`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 1.3 MB (1294694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128cee34993f6c191f293eb8726195324ee885bed43e321dae78c2d5a587fb8`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef60ac4e1282f8d5263cfd4dfb9c79a81dea7281fbb918a416e612c6d2598873`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 39.2 MB (39205981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992f744f5644cd6eaa8857bb9dbe0183992f21edf8be831e65a0d6a43d53eed`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e996c0ec018487718aa8c8b4101d230fde49e4b2f64e7b3b49ecae7e187c07`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 6.4 MB (6430464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ff921c60727ad35dc3d3e4e3ca80447343da2d0ee4e1d8460f1bf2409a190`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64b7573dd7428082c55d68ce5af8c9259740d0e341a3c2aec87acd86d6df32`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1222d11abbb4ea3cfb093b455e5588ce03875fa1cfb6113c4ec0c5a1cbac763c`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3882951f6afb4f316675d42e8a3e4b8dd88c05a8a754c9dcb3d64a12a066a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60aff89ba5a2e93bd4208b4befe75569964b442975cb9fc834639eee1177c1`

```dockerfile
```

-	Layers:
	-	`sha256:b4cf9b5f9b538b89a773bdcbfa035284cac0929226815dea238f80484048e28b`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 2.3 MB (2283083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e921159af6f57b2331258fbbe8e7b9da4f51b4f13b9d6cf2be40decdeed8c0a`  
		Last Modified: Tue, 17 Mar 2026 02:49:15 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:b48a22c6359bd460092ae16029c2367e65298eb946f9f0d6731aa8c168185fd1
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
$ docker pull fluentd@sha256:232406cf7372ec3334cc854604c6e4da073278562f45b4f4ba1999c1b0bdcb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79239187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160b4477cbc5df32a10ae2e9d2c1d4ace19b5e42149b80e2f51aebd182a1e0c8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:27:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:27:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:27:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:27:58 GMT
USER fluent
# Tue, 17 Mar 2026 00:27:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:27:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c59864e0006c1e4962cbce8eefb3283a4a8eb888aab9f56e43536f087a70ab6`  
		Last Modified: Mon, 16 Mar 2026 23:11:18 GMT  
		Size: 1.3 MB (1279856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1077cd177b7cad3d602a07fde8cfb1f7120cb3d374652b67b2366626493cc94`  
		Last Modified: Mon, 16 Mar 2026 23:11:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4661a3095708f309a1743a3b2d5b4c6ac368359732bef7c2b1dec88ad89c00`  
		Last Modified: Mon, 16 Mar 2026 23:11:19 GMT  
		Size: 42.1 MB (42127076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717106f0bff9cfbf1d8c00ef815c4c5644de7a6e65a46c00a7a94d924ae3e479`  
		Last Modified: Mon, 16 Mar 2026 23:11:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05e21871ed88ca83f56952ef1fff9d6eae302d6ef21e25a04a4145732b392a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 6.1 MB (6054358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d693447378ecf8530f5e5ba4e573500973fa2ee25516f6f4c73493cff4c3a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36446a00b3dd3da4571ffd45080ec39040b0d3bfe2b6384527c417b29faad2e`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec69e75e3840dc6f30a1545f3de12b3bfc3653e177637832c36a3daa695cf0`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fd5f1fdb922c52e7441ec9e197b3e3ade0d70dcbc15012914df9ca92b6ddbbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7490c1bacb57a4d23fa352fa126c44d28cfabb22fdc816b91b969a2edf28af9`

```dockerfile
```

-	Layers:
	-	`sha256:c324c52a2dd211e3dbe7b3a0ab4e53c4ba96377933843df7d1ed8da25fcab571`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33716a313882e7d53c0379971fd6063af2a9a08610bb4fec0845c7790dba0845`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f5e43113eaff653443d9485af541c538a37caf9500ddf2aea7ecdff67b09d32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73090231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21a8f68ce47cc615e162058a6ab896f49fcf0e82f8c9b1a04c94b5c146222a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:11:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:11:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:11:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:11:32 GMT
USER fluent
# Tue, 17 Mar 2026 01:11:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a43a05dbd3979d6f19a9eed8b3d0de971bfa48c3c53ec47d51d7b7bcb4651`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 1.3 MB (1263649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2e8340c868a18a42e59181f9d8524b24ea1dd6b85c2346ebbb407a777f0e2`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211628c31f1b196dd05de247142455ec46f19c2d0ae99be78daa53a1747f6b`  
		Last Modified: Mon, 16 Mar 2026 23:58:18 GMT  
		Size: 37.9 MB (37924120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b448d13fe704838615d979910c81e7aac357cc4dd21d7b73c4eda848c831b4`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9df04d3708ea4652201bd273e80ef0f6bfc99b6cc8462408fd0d0f5685495`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 6.0 MB (5956422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecae936460d331b4b75c996142043e42d708f3b1727e95470be7b050484f14`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13bd6b48910a2334b4b39b4cf38436333a627cf5e97e0bf0eac04769d22d5c5`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9953dd207b1750464e34f6ce106f085dd575c11dcb516b760b35fc889e938`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:587bf90da8db01a6f693c9e4d84096fa64788256ab664fa7f4ec715b74c87f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d7f001f823796cf988502e5dc9b8f1f3a425e12e51fa190711ff0dede0d51`

```dockerfile
```

-	Layers:
	-	`sha256:3eda4bfebd5a8a76c7f826675bd8b9e15729e7c87f6e528d7fd73f1723b0e7c8`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 2.3 MB (2284609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f01bb55871f9b063961672fcbba60c4e6b681e0e05784b2a619a05b266c17`  
		Last Modified: Tue, 17 Mar 2026 01:11:39 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5b1bb23084eef05385f4c4c74e3dd217d75777e06b82de8ad1b84ed3c07f6ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70954354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e1959aa1bb568fdba0c4711afeb0c4dcb57728ac7e5779b5de863c25d08ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:25:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:25:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:25:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:25:40 GMT
USER fluent
# Tue, 17 Mar 2026 01:25:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ce6cc2439c6b79c819ca9430e1bbb77c736ef2b35e42dd774e1ee18b76c924`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 1.2 MB (1237537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633f1380a4453313dbff0278ff9100b83a12c56bf46f93e6494d415adbf7156`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cdbd0c158a2b9bd3c2df11b9e6cbf24979873dcd4dc4f7ff1469aeb58e6cb`  
		Last Modified: Tue, 17 Mar 2026 00:29:18 GMT  
		Size: 37.8 MB (37780498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04683c59e4f85944be0b6ed9bd3f353decd8f53f54f32626c3936940fb9c16`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63790ca04810e0d66155f2f69b901211088284f5ac845b184cf0436e2c15f75`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 5.7 MB (5724425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa89e0a796adaa73e197d3004bd942194ca738139b01e37893e97c60bea10bd`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf7a0fc49c141a5d864b78aded16530a02f8b90eeb110e6a6560e4c68a8424`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e1c7b0665d871ae781d1de8b0072f804c50191b37acfd04efa02b8106960d`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c24a3a532f92707c6a93e6e8ca3e25c0cc1d5b674a6a71c4d04ae287fcb67f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52aba213be0f8322386168f1d2ec5f581cd3d9cace59f56cd117831b8aeb2911`

```dockerfile
```

-	Layers:
	-	`sha256:e832b0fade97830c666a9062f5a5907fc3c49b3b6623ccd210f8613aa92efc80`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 2.3 MB (2283050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f5bd3f3f0b9cab1b32cd827b01deeb8f18e2df01771c8634c82e9af4240afc`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7657694a7efdd9352062ca5978158d337bb1beff0e26592f6c8d9fa5ec2cfb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715de10dcb59a132e73255d71523d3a62f07f62af4100bdf83588d080a140936`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:28:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:28:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:28:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:28:13 GMT
USER fluent
# Tue, 17 Mar 2026 00:28:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:28:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92a159e78842706770d91322db2570dafe843687416a63a00f853632c63ea2`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 1.3 MB (1261719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bac3edea6f061f16806a6288d6e41577357f3b7b93e488a21e4a7fd4c0026`  
		Last Modified: Mon, 16 Mar 2026 23:16:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f3c5800da728b1d929316f1d9e7922cfd33a0e3837fe5894d84932d7b4bdb`  
		Last Modified: Mon, 16 Mar 2026 23:16:48 GMT  
		Size: 42.1 MB (42078629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f9cb2f0ffe8093241a96360434e49097b4e44d4920a83e5f8bdf651cb44d`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a14dcd72029447494a817832a7e07d7f37242f0dfc61fb95b94f9fd10ca15fe`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57138ce9a8b70f6c7a5d55a09bb75248aaec17efed7f25ade014241a289f6e`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf3ff271f286cbf184eba1d029d53f7e4d984c2f0fb7fd76a8a32cf87250fbc`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3052e2c628efed1916df587fc830bf2a5528dfc750a5bb474c8223c13e81ce`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c1e88a6ffa3097dc994d4e0991f7f47de295a837f1d4bf29cd561d95217f2be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c90d852e68a0d015595cbf540c9cae739255d59a789697fc41e328e2490548`

```dockerfile
```

-	Layers:
	-	`sha256:e7e9da00a2453346696d204f42c7112fce2e797a2b2a1b6654bfd3835d93a055`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 2.3 MB (2281910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf140398761f442be58afa79e717b45c4944cd5882049553aec402bda080eef1`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:c7d152b9229f3e070984e71e98c800db8e62995055254dcb3f735e3ef991ca17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76267475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2968d7815532be0e8410a27f1cf32e97d4f8af5d651e085d2f00ebe44644d82e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
CMD ["irb"]
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Mon, 16 Mar 2026 23:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 16 Mar 2026 23:58:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 16 Mar 2026 23:58:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 16 Mar 2026 23:58:39 GMT
USER fluent
# Mon, 16 Mar 2026 23:58:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 16 Mar 2026 23:58:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1da629cb883a06ff6b9ef25550345b4927b8b12f06fcbb138f2885887d1e03`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74c8124443e3a5d4ab3af6ec3c78c41fb6dbb305c9a75c723f91fb75b29a05`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab22c27d7d7daa338ddbae9eb6a91201dbaa87d3c9b68dfc028ad3827b4926`  
		Last Modified: Mon, 16 Mar 2026 23:09:48 GMT  
		Size: 37.7 MB (37660763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1abe2b804f27172a8dd698ff935138d6bf544d4bb4d5afe153b1cbab9a717`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4290f2b095cb17fa5d8f2928b201825b76a29726b003cd7b4d09ffaced3b1444`  
		Last Modified: Mon, 16 Mar 2026 23:58:47 GMT  
		Size: 6.0 MB (6025707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78becfe8530cd7d67f676ce149fec997d8bf0d1f12b5d84bbc78a82e5ce3088`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa13de4eb79e4748482048b2895633cd042c017b616f10bce785fbbd27921d56`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7f1df1b6474ed8750845743a45310fb4159c462d804c40a1dcfe3e04311bf`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:def4033cd1eb61c8f859e1fa1e99dd6b751a9a39975446bc009125d847856181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854c24027309a88546e818319a93806640f983b3ffa467e56c3ffed9b62ab973`

```dockerfile
```

-	Layers:
	-	`sha256:74ff77a8b1c990b237ac684de08321e9a1f26ca3191fa09144fb154662e3fce6`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 2.3 MB (2278826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06259fe209d39ca97315e79085c0e75719b4d6374d6481eee7a39e81f5d6d97a`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
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
$ docker pull fluentd@sha256:eea29c28ffa870cf2b759da9107723177e1872a7b4bb808acdd5824a14da0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76768794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7626f6e598ea93ab08fe91ea8e27b673ce3a92ce423257ab8469a1b9afec1ec1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 02:48:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 02:48:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 02:48:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 02:48:57 GMT
USER fluent
# Tue, 17 Mar 2026 02:48:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 02:48:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4fe3d99fd095b557f25c59245ba2eddb03ddc5040b30df042c597414c5f212`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 1.3 MB (1294694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128cee34993f6c191f293eb8726195324ee885bed43e321dae78c2d5a587fb8`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef60ac4e1282f8d5263cfd4dfb9c79a81dea7281fbb918a416e612c6d2598873`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 39.2 MB (39205981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992f744f5644cd6eaa8857bb9dbe0183992f21edf8be831e65a0d6a43d53eed`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e996c0ec018487718aa8c8b4101d230fde49e4b2f64e7b3b49ecae7e187c07`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 6.4 MB (6430464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ff921c60727ad35dc3d3e4e3ca80447343da2d0ee4e1d8460f1bf2409a190`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64b7573dd7428082c55d68ce5af8c9259740d0e341a3c2aec87acd86d6df32`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1222d11abbb4ea3cfb093b455e5588ce03875fa1cfb6113c4ec0c5a1cbac763c`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3882951f6afb4f316675d42e8a3e4b8dd88c05a8a754c9dcb3d64a12a066a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60aff89ba5a2e93bd4208b4befe75569964b442975cb9fc834639eee1177c1`

```dockerfile
```

-	Layers:
	-	`sha256:b4cf9b5f9b538b89a773bdcbfa035284cac0929226815dea238f80484048e28b`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 2.3 MB (2283083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e921159af6f57b2331258fbbe8e7b9da4f51b4f13b9d6cf2be40decdeed8c0a`  
		Last Modified: Tue, 17 Mar 2026 02:49:15 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:b48a22c6359bd460092ae16029c2367e65298eb946f9f0d6731aa8c168185fd1
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
$ docker pull fluentd@sha256:232406cf7372ec3334cc854604c6e4da073278562f45b4f4ba1999c1b0bdcb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79239187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160b4477cbc5df32a10ae2e9d2c1d4ace19b5e42149b80e2f51aebd182a1e0c8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:27:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:27:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:27:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:27:58 GMT
USER fluent
# Tue, 17 Mar 2026 00:27:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:27:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c59864e0006c1e4962cbce8eefb3283a4a8eb888aab9f56e43536f087a70ab6`  
		Last Modified: Mon, 16 Mar 2026 23:11:18 GMT  
		Size: 1.3 MB (1279856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1077cd177b7cad3d602a07fde8cfb1f7120cb3d374652b67b2366626493cc94`  
		Last Modified: Mon, 16 Mar 2026 23:11:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4661a3095708f309a1743a3b2d5b4c6ac368359732bef7c2b1dec88ad89c00`  
		Last Modified: Mon, 16 Mar 2026 23:11:19 GMT  
		Size: 42.1 MB (42127076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717106f0bff9cfbf1d8c00ef815c4c5644de7a6e65a46c00a7a94d924ae3e479`  
		Last Modified: Mon, 16 Mar 2026 23:11:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05e21871ed88ca83f56952ef1fff9d6eae302d6ef21e25a04a4145732b392a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 6.1 MB (6054358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d693447378ecf8530f5e5ba4e573500973fa2ee25516f6f4c73493cff4c3a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36446a00b3dd3da4571ffd45080ec39040b0d3bfe2b6384527c417b29faad2e`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec69e75e3840dc6f30a1545f3de12b3bfc3653e177637832c36a3daa695cf0`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fd5f1fdb922c52e7441ec9e197b3e3ade0d70dcbc15012914df9ca92b6ddbbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7490c1bacb57a4d23fa352fa126c44d28cfabb22fdc816b91b969a2edf28af9`

```dockerfile
```

-	Layers:
	-	`sha256:c324c52a2dd211e3dbe7b3a0ab4e53c4ba96377933843df7d1ed8da25fcab571`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33716a313882e7d53c0379971fd6063af2a9a08610bb4fec0845c7790dba0845`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f5e43113eaff653443d9485af541c538a37caf9500ddf2aea7ecdff67b09d32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73090231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21a8f68ce47cc615e162058a6ab896f49fcf0e82f8c9b1a04c94b5c146222a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:11:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:11:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:11:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:11:32 GMT
USER fluent
# Tue, 17 Mar 2026 01:11:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a43a05dbd3979d6f19a9eed8b3d0de971bfa48c3c53ec47d51d7b7bcb4651`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 1.3 MB (1263649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2e8340c868a18a42e59181f9d8524b24ea1dd6b85c2346ebbb407a777f0e2`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211628c31f1b196dd05de247142455ec46f19c2d0ae99be78daa53a1747f6b`  
		Last Modified: Mon, 16 Mar 2026 23:58:18 GMT  
		Size: 37.9 MB (37924120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b448d13fe704838615d979910c81e7aac357cc4dd21d7b73c4eda848c831b4`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9df04d3708ea4652201bd273e80ef0f6bfc99b6cc8462408fd0d0f5685495`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 6.0 MB (5956422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecae936460d331b4b75c996142043e42d708f3b1727e95470be7b050484f14`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13bd6b48910a2334b4b39b4cf38436333a627cf5e97e0bf0eac04769d22d5c5`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9953dd207b1750464e34f6ce106f085dd575c11dcb516b760b35fc889e938`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:587bf90da8db01a6f693c9e4d84096fa64788256ab664fa7f4ec715b74c87f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d7f001f823796cf988502e5dc9b8f1f3a425e12e51fa190711ff0dede0d51`

```dockerfile
```

-	Layers:
	-	`sha256:3eda4bfebd5a8a76c7f826675bd8b9e15729e7c87f6e528d7fd73f1723b0e7c8`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 2.3 MB (2284609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f01bb55871f9b063961672fcbba60c4e6b681e0e05784b2a619a05b266c17`  
		Last Modified: Tue, 17 Mar 2026 01:11:39 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5b1bb23084eef05385f4c4c74e3dd217d75777e06b82de8ad1b84ed3c07f6ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70954354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e1959aa1bb568fdba0c4711afeb0c4dcb57728ac7e5779b5de863c25d08ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:25:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:25:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:25:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:25:40 GMT
USER fluent
# Tue, 17 Mar 2026 01:25:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ce6cc2439c6b79c819ca9430e1bbb77c736ef2b35e42dd774e1ee18b76c924`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 1.2 MB (1237537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633f1380a4453313dbff0278ff9100b83a12c56bf46f93e6494d415adbf7156`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cdbd0c158a2b9bd3c2df11b9e6cbf24979873dcd4dc4f7ff1469aeb58e6cb`  
		Last Modified: Tue, 17 Mar 2026 00:29:18 GMT  
		Size: 37.8 MB (37780498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04683c59e4f85944be0b6ed9bd3f353decd8f53f54f32626c3936940fb9c16`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63790ca04810e0d66155f2f69b901211088284f5ac845b184cf0436e2c15f75`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 5.7 MB (5724425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa89e0a796adaa73e197d3004bd942194ca738139b01e37893e97c60bea10bd`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf7a0fc49c141a5d864b78aded16530a02f8b90eeb110e6a6560e4c68a8424`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e1c7b0665d871ae781d1de8b0072f804c50191b37acfd04efa02b8106960d`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c24a3a532f92707c6a93e6e8ca3e25c0cc1d5b674a6a71c4d04ae287fcb67f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52aba213be0f8322386168f1d2ec5f581cd3d9cace59f56cd117831b8aeb2911`

```dockerfile
```

-	Layers:
	-	`sha256:e832b0fade97830c666a9062f5a5907fc3c49b3b6623ccd210f8613aa92efc80`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 2.3 MB (2283050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f5bd3f3f0b9cab1b32cd827b01deeb8f18e2df01771c8634c82e9af4240afc`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7657694a7efdd9352062ca5978158d337bb1beff0e26592f6c8d9fa5ec2cfb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715de10dcb59a132e73255d71523d3a62f07f62af4100bdf83588d080a140936`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:28:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:28:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:28:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:28:13 GMT
USER fluent
# Tue, 17 Mar 2026 00:28:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:28:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92a159e78842706770d91322db2570dafe843687416a63a00f853632c63ea2`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 1.3 MB (1261719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bac3edea6f061f16806a6288d6e41577357f3b7b93e488a21e4a7fd4c0026`  
		Last Modified: Mon, 16 Mar 2026 23:16:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f3c5800da728b1d929316f1d9e7922cfd33a0e3837fe5894d84932d7b4bdb`  
		Last Modified: Mon, 16 Mar 2026 23:16:48 GMT  
		Size: 42.1 MB (42078629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f9cb2f0ffe8093241a96360434e49097b4e44d4920a83e5f8bdf651cb44d`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a14dcd72029447494a817832a7e07d7f37242f0dfc61fb95b94f9fd10ca15fe`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57138ce9a8b70f6c7a5d55a09bb75248aaec17efed7f25ade014241a289f6e`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf3ff271f286cbf184eba1d029d53f7e4d984c2f0fb7fd76a8a32cf87250fbc`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3052e2c628efed1916df587fc830bf2a5528dfc750a5bb474c8223c13e81ce`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c1e88a6ffa3097dc994d4e0991f7f47de295a837f1d4bf29cd561d95217f2be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c90d852e68a0d015595cbf540c9cae739255d59a789697fc41e328e2490548`

```dockerfile
```

-	Layers:
	-	`sha256:e7e9da00a2453346696d204f42c7112fce2e797a2b2a1b6654bfd3835d93a055`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 2.3 MB (2281910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf140398761f442be58afa79e717b45c4944cd5882049553aec402bda080eef1`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c7d152b9229f3e070984e71e98c800db8e62995055254dcb3f735e3ef991ca17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76267475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2968d7815532be0e8410a27f1cf32e97d4f8af5d651e085d2f00ebe44644d82e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
CMD ["irb"]
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Mon, 16 Mar 2026 23:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 16 Mar 2026 23:58:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 16 Mar 2026 23:58:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 16 Mar 2026 23:58:39 GMT
USER fluent
# Mon, 16 Mar 2026 23:58:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 16 Mar 2026 23:58:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1da629cb883a06ff6b9ef25550345b4927b8b12f06fcbb138f2885887d1e03`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74c8124443e3a5d4ab3af6ec3c78c41fb6dbb305c9a75c723f91fb75b29a05`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab22c27d7d7daa338ddbae9eb6a91201dbaa87d3c9b68dfc028ad3827b4926`  
		Last Modified: Mon, 16 Mar 2026 23:09:48 GMT  
		Size: 37.7 MB (37660763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1abe2b804f27172a8dd698ff935138d6bf544d4bb4d5afe153b1cbab9a717`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4290f2b095cb17fa5d8f2928b201825b76a29726b003cd7b4d09ffaced3b1444`  
		Last Modified: Mon, 16 Mar 2026 23:58:47 GMT  
		Size: 6.0 MB (6025707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78becfe8530cd7d67f676ce149fec997d8bf0d1f12b5d84bbc78a82e5ce3088`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa13de4eb79e4748482048b2895633cd042c017b616f10bce785fbbd27921d56`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7f1df1b6474ed8750845743a45310fb4159c462d804c40a1dcfe3e04311bf`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:def4033cd1eb61c8f859e1fa1e99dd6b751a9a39975446bc009125d847856181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854c24027309a88546e818319a93806640f983b3ffa467e56c3ffed9b62ab973`

```dockerfile
```

-	Layers:
	-	`sha256:74ff77a8b1c990b237ac684de08321e9a1f26ca3191fa09144fb154662e3fce6`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 2.3 MB (2278826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06259fe209d39ca97315e79085c0e75719b4d6374d6481eee7a39e81f5d6d97a`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
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
$ docker pull fluentd@sha256:eea29c28ffa870cf2b759da9107723177e1872a7b4bb808acdd5824a14da0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76768794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7626f6e598ea93ab08fe91ea8e27b673ce3a92ce423257ab8469a1b9afec1ec1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 02:48:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 02:48:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 02:48:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 02:48:57 GMT
USER fluent
# Tue, 17 Mar 2026 02:48:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 02:48:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4fe3d99fd095b557f25c59245ba2eddb03ddc5040b30df042c597414c5f212`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 1.3 MB (1294694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128cee34993f6c191f293eb8726195324ee885bed43e321dae78c2d5a587fb8`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef60ac4e1282f8d5263cfd4dfb9c79a81dea7281fbb918a416e612c6d2598873`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 39.2 MB (39205981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992f744f5644cd6eaa8857bb9dbe0183992f21edf8be831e65a0d6a43d53eed`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e996c0ec018487718aa8c8b4101d230fde49e4b2f64e7b3b49ecae7e187c07`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 6.4 MB (6430464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ff921c60727ad35dc3d3e4e3ca80447343da2d0ee4e1d8460f1bf2409a190`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64b7573dd7428082c55d68ce5af8c9259740d0e341a3c2aec87acd86d6df32`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1222d11abbb4ea3cfb093b455e5588ce03875fa1cfb6113c4ec0c5a1cbac763c`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3882951f6afb4f316675d42e8a3e4b8dd88c05a8a754c9dcb3d64a12a066a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60aff89ba5a2e93bd4208b4befe75569964b442975cb9fc834639eee1177c1`

```dockerfile
```

-	Layers:
	-	`sha256:b4cf9b5f9b538b89a773bdcbfa035284cac0929226815dea238f80484048e28b`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 2.3 MB (2283083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e921159af6f57b2331258fbbe8e7b9da4f51b4f13b9d6cf2be40decdeed8c0a`  
		Last Modified: Tue, 17 Mar 2026 02:49:15 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:b48a22c6359bd460092ae16029c2367e65298eb946f9f0d6731aa8c168185fd1
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
$ docker pull fluentd@sha256:232406cf7372ec3334cc854604c6e4da073278562f45b4f4ba1999c1b0bdcb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79239187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160b4477cbc5df32a10ae2e9d2c1d4ace19b5e42149b80e2f51aebd182a1e0c8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:08:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:11:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:11:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:11:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:11:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:27:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:27:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:27:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:27:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:27:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:27:58 GMT
USER fluent
# Tue, 17 Mar 2026 00:27:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:27:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c59864e0006c1e4962cbce8eefb3283a4a8eb888aab9f56e43536f087a70ab6`  
		Last Modified: Mon, 16 Mar 2026 23:11:18 GMT  
		Size: 1.3 MB (1279856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1077cd177b7cad3d602a07fde8cfb1f7120cb3d374652b67b2366626493cc94`  
		Last Modified: Mon, 16 Mar 2026 23:11:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4661a3095708f309a1743a3b2d5b4c6ac368359732bef7c2b1dec88ad89c00`  
		Last Modified: Mon, 16 Mar 2026 23:11:19 GMT  
		Size: 42.1 MB (42127076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717106f0bff9cfbf1d8c00ef815c4c5644de7a6e65a46c00a7a94d924ae3e479`  
		Last Modified: Mon, 16 Mar 2026 23:11:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05e21871ed88ca83f56952ef1fff9d6eae302d6ef21e25a04a4145732b392a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 6.1 MB (6054358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d693447378ecf8530f5e5ba4e573500973fa2ee25516f6f4c73493cff4c3a`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36446a00b3dd3da4571ffd45080ec39040b0d3bfe2b6384527c417b29faad2e`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec69e75e3840dc6f30a1545f3de12b3bfc3653e177637832c36a3daa695cf0`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fd5f1fdb922c52e7441ec9e197b3e3ade0d70dcbc15012914df9ca92b6ddbbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7490c1bacb57a4d23fa352fa126c44d28cfabb22fdc816b91b969a2edf28af9`

```dockerfile
```

-	Layers:
	-	`sha256:c324c52a2dd211e3dbe7b3a0ab4e53c4ba96377933843df7d1ed8da25fcab571`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33716a313882e7d53c0379971fd6063af2a9a08610bb4fec0845c7790dba0845`  
		Last Modified: Tue, 17 Mar 2026 00:28:06 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f5e43113eaff653443d9485af541c538a37caf9500ddf2aea7ecdff67b09d32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73090231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21a8f68ce47cc615e162058a6ab896f49fcf0e82f8c9b1a04c94b5c146222a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:55:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:58:09 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:58:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:58:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:58:09 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:11:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:11:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:11:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:11:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:11:32 GMT
USER fluent
# Tue, 17 Mar 2026 01:11:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:11:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a43a05dbd3979d6f19a9eed8b3d0de971bfa48c3c53ec47d51d7b7bcb4651`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 1.3 MB (1263649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2e8340c868a18a42e59181f9d8524b24ea1dd6b85c2346ebbb407a777f0e2`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211628c31f1b196dd05de247142455ec46f19c2d0ae99be78daa53a1747f6b`  
		Last Modified: Mon, 16 Mar 2026 23:58:18 GMT  
		Size: 37.9 MB (37924120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b448d13fe704838615d979910c81e7aac357cc4dd21d7b73c4eda848c831b4`  
		Last Modified: Mon, 16 Mar 2026 23:58:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9df04d3708ea4652201bd273e80ef0f6bfc99b6cc8462408fd0d0f5685495`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 6.0 MB (5956422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecae936460d331b4b75c996142043e42d708f3b1727e95470be7b050484f14`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13bd6b48910a2334b4b39b4cf38436333a627cf5e97e0bf0eac04769d22d5c5`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9953dd207b1750464e34f6ce106f085dd575c11dcb516b760b35fc889e938`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:587bf90da8db01a6f693c9e4d84096fa64788256ab664fa7f4ec715b74c87f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d7f001f823796cf988502e5dc9b8f1f3a425e12e51fa190711ff0dede0d51`

```dockerfile
```

-	Layers:
	-	`sha256:3eda4bfebd5a8a76c7f826675bd8b9e15729e7c87f6e528d7fd73f1723b0e7c8`  
		Last Modified: Tue, 17 Mar 2026 01:11:40 GMT  
		Size: 2.3 MB (2284609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f01bb55871f9b063961672fcbba60c4e6b681e0e05784b2a619a05b266c17`  
		Last Modified: Tue, 17 Mar 2026 01:11:39 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5b1bb23084eef05385f4c4c74e3dd217d75777e06b82de8ad1b84ed3c07f6ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70954354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e1959aa1bb568fdba0c4711afeb0c4dcb57728ac7e5779b5de863c25d08ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:26:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 00:29:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 00:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:29:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 00:29:08 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 01:25:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 01:25:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 01:25:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 01:25:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 01:25:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 01:25:40 GMT
USER fluent
# Tue, 17 Mar 2026 01:25:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ce6cc2439c6b79c819ca9430e1bbb77c736ef2b35e42dd774e1ee18b76c924`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 1.2 MB (1237537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633f1380a4453313dbff0278ff9100b83a12c56bf46f93e6494d415adbf7156`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cdbd0c158a2b9bd3c2df11b9e6cbf24979873dcd4dc4f7ff1469aeb58e6cb`  
		Last Modified: Tue, 17 Mar 2026 00:29:18 GMT  
		Size: 37.8 MB (37780498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04683c59e4f85944be0b6ed9bd3f353decd8f53f54f32626c3936940fb9c16`  
		Last Modified: Tue, 17 Mar 2026 00:29:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63790ca04810e0d66155f2f69b901211088284f5ac845b184cf0436e2c15f75`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 5.7 MB (5724425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa89e0a796adaa73e197d3004bd942194ca738139b01e37893e97c60bea10bd`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf7a0fc49c141a5d864b78aded16530a02f8b90eeb110e6a6560e4c68a8424`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e1c7b0665d871ae781d1de8b0072f804c50191b37acfd04efa02b8106960d`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c24a3a532f92707c6a93e6e8ca3e25c0cc1d5b674a6a71c4d04ae287fcb67f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52aba213be0f8322386168f1d2ec5f581cd3d9cace59f56cd117831b8aeb2911`

```dockerfile
```

-	Layers:
	-	`sha256:e832b0fade97830c666a9062f5a5907fc3c49b3b6623ccd210f8613aa92efc80`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 2.3 MB (2283050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f5bd3f3f0b9cab1b32cd827b01deeb8f18e2df01771c8634c82e9af4240afc`  
		Last Modified: Tue, 17 Mar 2026 01:25:48 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7657694a7efdd9352062ca5978158d337bb1beff0e26592f6c8d9fa5ec2cfb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715de10dcb59a132e73255d71523d3a62f07f62af4100bdf83588d080a140936`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:14:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:16:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:16:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:16:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:16:38 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 00:28:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 00:28:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 00:28:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 00:28:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 00:28:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 00:28:13 GMT
USER fluent
# Tue, 17 Mar 2026 00:28:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 00:28:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92a159e78842706770d91322db2570dafe843687416a63a00f853632c63ea2`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 1.3 MB (1261719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bac3edea6f061f16806a6288d6e41577357f3b7b93e488a21e4a7fd4c0026`  
		Last Modified: Mon, 16 Mar 2026 23:16:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f3c5800da728b1d929316f1d9e7922cfd33a0e3837fe5894d84932d7b4bdb`  
		Last Modified: Mon, 16 Mar 2026 23:16:48 GMT  
		Size: 42.1 MB (42078629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49f9cb2f0ffe8093241a96360434e49097b4e44d4920a83e5f8bdf651cb44d`  
		Last Modified: Mon, 16 Mar 2026 23:16:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a14dcd72029447494a817832a7e07d7f37242f0dfc61fb95b94f9fd10ca15fe`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 6.0 MB (6044154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57138ce9a8b70f6c7a5d55a09bb75248aaec17efed7f25ade014241a289f6e`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf3ff271f286cbf184eba1d029d53f7e4d984c2f0fb7fd76a8a32cf87250fbc`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3052e2c628efed1916df587fc830bf2a5528dfc750a5bb474c8223c13e81ce`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c1e88a6ffa3097dc994d4e0991f7f47de295a837f1d4bf29cd561d95217f2be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c90d852e68a0d015595cbf540c9cae739255d59a789697fc41e328e2490548`

```dockerfile
```

-	Layers:
	-	`sha256:e7e9da00a2453346696d204f42c7112fce2e797a2b2a1b6654bfd3835d93a055`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 2.3 MB (2281910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf140398761f442be58afa79e717b45c4944cd5882049553aec402bda080eef1`  
		Last Modified: Tue, 17 Mar 2026 00:28:21 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c7d152b9229f3e070984e71e98c800db8e62995055254dcb3f735e3ef991ca17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76267475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2968d7815532be0e8410a27f1cf32e97d4f8af5d651e085d2f00ebe44644d82e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:07:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_VERSION=3.4.9
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Mon, 16 Mar 2026 23:09:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 16 Mar 2026 23:09:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:09:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 16 Mar 2026 23:09:39 GMT
CMD ["irb"]
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 16 Mar 2026 23:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Mon, 16 Mar 2026 23:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 16 Mar 2026 23:58:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 16 Mar 2026 23:58:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 16 Mar 2026 23:58:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 16 Mar 2026 23:58:39 GMT
USER fluent
# Mon, 16 Mar 2026 23:58:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 16 Mar 2026 23:58:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1da629cb883a06ff6b9ef25550345b4927b8b12f06fcbb138f2885887d1e03`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74c8124443e3a5d4ab3af6ec3c78c41fb6dbb305c9a75c723f91fb75b29a05`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab22c27d7d7daa338ddbae9eb6a91201dbaa87d3c9b68dfc028ad3827b4926`  
		Last Modified: Mon, 16 Mar 2026 23:09:48 GMT  
		Size: 37.7 MB (37660763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1abe2b804f27172a8dd698ff935138d6bf544d4bb4d5afe153b1cbab9a717`  
		Last Modified: Mon, 16 Mar 2026 23:09:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4290f2b095cb17fa5d8f2928b201825b76a29726b003cd7b4d09ffaced3b1444`  
		Last Modified: Mon, 16 Mar 2026 23:58:47 GMT  
		Size: 6.0 MB (6025707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78becfe8530cd7d67f676ce149fec997d8bf0d1f12b5d84bbc78a82e5ce3088`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa13de4eb79e4748482048b2895633cd042c017b616f10bce785fbbd27921d56`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7f1df1b6474ed8750845743a45310fb4159c462d804c40a1dcfe3e04311bf`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:def4033cd1eb61c8f859e1fa1e99dd6b751a9a39975446bc009125d847856181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854c24027309a88546e818319a93806640f983b3ffa467e56c3ffed9b62ab973`

```dockerfile
```

-	Layers:
	-	`sha256:74ff77a8b1c990b237ac684de08321e9a1f26ca3191fa09144fb154662e3fce6`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
		Size: 2.3 MB (2278826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06259fe209d39ca97315e79085c0e75719b4d6374d6481eee7a39e81f5d6d97a`  
		Last Modified: Mon, 16 Mar 2026 23:58:46 GMT  
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
$ docker pull fluentd@sha256:eea29c28ffa870cf2b759da9107723177e1872a7b4bb808acdd5824a14da0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76768794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7626f6e598ea93ab08fe91ea8e27b673ce3a92ce423257ab8469a1b9afec1ec1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:11:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 01:14:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 01:14:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:14:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 01:14:37 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 02:48:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 02:48:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 02:48:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 02:48:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 02:48:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 02:48:57 GMT
USER fluent
# Tue, 17 Mar 2026 02:48:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 02:48:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4fe3d99fd095b557f25c59245ba2eddb03ddc5040b30df042c597414c5f212`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 1.3 MB (1294694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128cee34993f6c191f293eb8726195324ee885bed43e321dae78c2d5a587fb8`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef60ac4e1282f8d5263cfd4dfb9c79a81dea7281fbb918a416e612c6d2598873`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 39.2 MB (39205981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992f744f5644cd6eaa8857bb9dbe0183992f21edf8be831e65a0d6a43d53eed`  
		Last Modified: Tue, 17 Mar 2026 01:14:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e996c0ec018487718aa8c8b4101d230fde49e4b2f64e7b3b49ecae7e187c07`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 6.4 MB (6430464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ff921c60727ad35dc3d3e4e3ca80447343da2d0ee4e1d8460f1bf2409a190`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64b7573dd7428082c55d68ce5af8c9259740d0e341a3c2aec87acd86d6df32`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1222d11abbb4ea3cfb093b455e5588ce03875fa1cfb6113c4ec0c5a1cbac763c`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3882951f6afb4f316675d42e8a3e4b8dd88c05a8a754c9dcb3d64a12a066a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad60aff89ba5a2e93bd4208b4befe75569964b442975cb9fc834639eee1177c1`

```dockerfile
```

-	Layers:
	-	`sha256:b4cf9b5f9b538b89a773bdcbfa035284cac0929226815dea238f80484048e28b`  
		Last Modified: Tue, 17 Mar 2026 02:49:16 GMT  
		Size: 2.3 MB (2283083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e921159af6f57b2331258fbbe8e7b9da4f51b4f13b9d6cf2be40decdeed8c0a`  
		Last Modified: Tue, 17 Mar 2026 02:49:15 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
