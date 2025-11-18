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
$ docker pull fluentd@sha256:8cf29dd79923e5b563ae2095db9db02320afa4da54e353acc0909e48c9ad4598
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
$ docker pull fluentd@sha256:7819416a79c16651791d8bc33c3d2d2bacccae796b2d58770eef22cae6934ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79263253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c2fd4acd09b8114f6adaad9f0a061339841357d75b38302a422e22d2cf71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 07:56:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 07:56:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 07:56:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 07:56:47 GMT
USER fluent
# Tue, 04 Nov 2025 07:56:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16a280ca2b46af513537a7d977a24dd0779f3b6b7ac2a379e32564f36bb62f`  
		Last Modified: Tue, 04 Nov 2025 04:29:35 GMT  
		Size: 1.3 MB (1279642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12677bb7810189f862e4324fd378db9bc131cf8446805bdcf9923ad09d03c85`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e12593a63e3781635232c1a24a87ca6d97150b8e568eaf8b52786ec55eeb71`  
		Last Modified: Tue, 04 Nov 2025 04:29:38 GMT  
		Size: 42.2 MB (42158201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06499c8b4d3f65803507338e343bb0c0eb7ef53c593e6346ab9acb506fd6234`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27dc8130de8c329d0a0c9f1c320445f464a342eeb7f063813ab0795d768eab1`  
		Last Modified: Tue, 04 Nov 2025 07:57:02 GMT  
		Size: 6.0 MB (6044919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84612fac3accfb10321a8fe2ca5683b31586a4b08497cd6e4d5fc2af03946b74`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95792bf9a95a58f0406cece5a0f922c7a14b54d4f7b0df84dec66681318c7f`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a524cc95e962099ab0a7ea84fc877a450f98399087903f4f5952648f8103d1`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:a15d99c368e421dc0bec89ac4bea53a7b5e3fb28994944ce9205dca48d2661b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964096aad19d9289aacb375444671cad9a090d9c902fe5aad199190dcc630703`

```dockerfile
```

-	Layers:
	-	`sha256:6918ed07569ebd6b8095f181ae6eb385f22aa81af468c74a7e0b6e6e30d1e9ce`  
		Last Modified: Tue, 04 Nov 2025 09:28:27 GMT  
		Size: 2.3 MB (2283564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed68f47f9b6c0beb0b780aac2d7d516a0badcbf467db435bde84defa983cdd8`  
		Last Modified: Tue, 04 Nov 2025 09:28:28 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
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
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
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
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:544e4c0d4869ab3260580ecc06084b2ced7e4a6f01a2241d3dcc84aff57415a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce55aad25aee0631fc7e542c25999e2a3222438f483fe8a8070a7dcb9c49f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 03:44:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:44:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:44:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:44:57 GMT
USER fluent
# Tue, 04 Nov 2025 03:44:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff1cf61353f8dff587184978fed1cbb398dca8e140da33c564fefaec487d2e`  
		Last Modified: Tue, 04 Nov 2025 02:36:44 GMT  
		Size: 1.2 MB (1236604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff3a12ca516b6f79cbac115ae27bcbb967dd1009cccff770d79a7cae383a3f`  
		Last Modified: Tue, 04 Nov 2025 02:36:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6468f7034188523d195654f6c0fb84c8d7d944289ae9e8f031cb5f78c7a580`  
		Last Modified: Tue, 04 Nov 2025 02:39:45 GMT  
		Size: 37.9 MB (37865491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950069925d30b01ded0a2ed186d917f1eff55fd5881f4be0b9d79cf4398aee27`  
		Last Modified: Tue, 04 Nov 2025 02:39:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861110680e1af462aee0aeffd9bb605f97301dfbacee73847bdbbfc8d45eff00`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 5.7 MB (5706065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9eeb05f20b9801ce1491ceac4a4721fad3184d46b7e5829d4ea70dec205204`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cf759dc69023991dabc97ed97c90d836d0080e04dc6e31eee3154c3e63bc`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaee8cdfbeb1c9562699525af9ea90ae4fb972270008cf3c8d09afce225ff4d`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:81151156ca085b78155762060cf4e8475f93f3c8a634c3fc05b75eaf2f1cbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42bb9185d066277fd1c662f181dd3d98d74f982179b66658d8044bd8483a68a`

```dockerfile
```

-	Layers:
	-	`sha256:b1d298e7774fea3ebb0f378680fd9fe5a7227345f1e92d8a8f5bb7561b0230f9`  
		Last Modified: Tue, 04 Nov 2025 12:28:29 GMT  
		Size: 2.3 MB (2284976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f942b31474bfce92005254c89e81053a0b334f42328c9c7b3ebd0d56bd8c2606`  
		Last Modified: Tue, 04 Nov 2025 12:28:30 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:91b6b4da2fc6090374e0fda11e524d15864879c72ab8ea891305c6a5dcc6f8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79582515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7ede2b923eb0046c874d79a45ff044f0476e7c68dc32b7025c20e8b4e2e79e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 02:37:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 02:37:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 02:37:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 02:37:13 GMT
USER fluent
# Tue, 04 Nov 2025 02:37:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 02:37:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c83755afbe771e645a69fd11df0a60d6e7dd541fc57e5b0f1b0be4b2a0883`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 1.3 MB (1261429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c48599929aa6c7fb7bed5f82a13c0154ffb885b6f1e85e9f644b0767b1f70`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e552b7b884adedf291e273039ac04ca2d02aac2bf91d0790d8ed1417002926`  
		Last Modified: Tue, 04 Nov 2025 01:42:15 GMT  
		Size: 42.1 MB (42145432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35feb980ed30f707dcd311800ab0801ef0c69e411a8513d2d57f4e74def26a3`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3b50e47c048e589ed069424290b2dadff117a2cfb2306543d6ea53432fdb`  
		Last Modified: Tue, 04 Nov 2025 02:37:29 GMT  
		Size: 6.0 MB (6030973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb7f246be820a9a7035411437ec82adb7b7e57751074a838dcb8b57853e218`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fee3af5dc401f90c63aff5571b43de11c5e287af015286ceac268d59823fb`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b82136c4c34e431e87e862f28be1d30faf08715c8265f07c8c6c3f747472b0`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:12d71120b81b51551d597b9ce196c3ad25405bb7534bb306d9695e728dbe357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184e9b9694fc38927b46e669811d5a4188b127fdbfb32a2c12b823816eb472b3`

```dockerfile
```

-	Layers:
	-	`sha256:9af4c91c515dc26f2329814b50546b04473222e4ebe2c4a0c84c607529966896`  
		Last Modified: Tue, 04 Nov 2025 12:28:33 GMT  
		Size: 2.3 MB (2283836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff4bfd853e2bbafcd8a04cb7af0cf640464cbeddc807c9e1758691418aa7f0d`  
		Last Modified: Tue, 04 Nov 2025 12:28:34 GMT  
		Size: 21.2 KB (21231 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
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
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
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
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0394134b4106e1a322bc5bea388bc8ea50ff54a9ec059144495d0a36ce1895e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81071254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4416a657be5c504ac27d0c7cfc006b240f8440de7467c80ea69c3bc92deb14`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:16:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:30:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:30:05 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 19:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:58:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:58:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:58:41 GMT
USER fluent
# Tue, 04 Nov 2025 19:58:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:58:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7cafc9e521290ae17ae96071a62fa0ce9cc48a489bf957fdf15c09abb8a804`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 1.3 MB (1310384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74df3c614cf044979896d45fdbb3780600a0f2a6f1a699a70de10d0153e6928`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312abe5d4cfc4eeefc5f2b09f01e9ba77dc6e592a8edc74346d8a87f2e45f28`  
		Last Modified: Tue, 04 Nov 2025 12:31:03 GMT  
		Size: 39.6 MB (39601068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf418f7fe1d0352a8b07d3730b4a8393da06df977da19a9696aee08825025762`  
		Last Modified: Tue, 04 Nov 2025 12:31:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091f8580ca0d0137a62e83860303b48b10b634f2bf8c18920dc53938f130c40`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 6.6 MB (6558759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718bc6b50d295b1fd485e209c3ff74421802ebc3cf2cef01b33cb7da8e34b56d`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd40aa235056c26c6f0ae37c8933e1bb288034d9df402cc18252f6469055634`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7206d908d6189a487af234889268cf4d47da74c4477a00e4cfd36716b4da41`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fae67ad3e796f6f0ecc8f62eb44739b84e730d986fd6ad5f24529f7d2d9f5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb05857bad1224261621c7abf7b6d6c484c2426724863ca259d07ec32a30073`

```dockerfile
```

-	Layers:
	-	`sha256:c37622be462407f9cc248533cbe5481f7f58bdfa498235b22b4fa1c6d44c5e02`  
		Last Modified: Tue, 04 Nov 2025 21:28:33 GMT  
		Size: 2.3 MB (2287099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb120fc15050a9d25f652c7c39a98e10d98d3dcaff6ec871e1c195547104024d`  
		Last Modified: Tue, 04 Nov 2025 21:28:34 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:1ba5ab678ead4498d917c4a7acd915ded9543f724cca2e527022ac6d159ca302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76838773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b70ec958c85adaa042b79d68f9db29879abdda7e2a6d46e6a9abd70dcff705`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:39:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:46:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:46:17 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 16:53:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:53:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:53:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:53:20 GMT
USER fluent
# Tue, 04 Nov 2025 16:53:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:53:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc87d0d125756f6f7207ff00dd475820f1f662c1490e4f973570b5313e17fb6`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 1.3 MB (1294636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7ffedbe0c72a7402c4c7ffa7ad05e05878b479406400dca12509798aee65e`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f9a0ba0eb1a5da7986fb92d450451bc333572015535b1b763a366214e8b6b`  
		Last Modified: Tue, 04 Nov 2025 12:47:04 GMT  
		Size: 39.3 MB (39287395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46ca528085c3652d506f94d3950096f37aeec2bac6827ae4ff7383b0116b3a`  
		Last Modified: Tue, 04 Nov 2025 12:47:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa746dbbf4325707691bffabcca7d685a3cc3583cfe8ab8fbf04e6277f7aa0`  
		Last Modified: Tue, 04 Nov 2025 16:53:53 GMT  
		Size: 6.4 MB (6416957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8612a12f56f9dd86f9543a9f598cbf2d6a78e2b2142aa806819ba55ce2e4c`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9830c4ec73592c4e33e871e27ce42c0d59915736cb3509bce80fa989224d30d4`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5636653a1ba6f2e97b635e9f1431d02cdd51383519faadd8db32a4d63b5c29`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc22a7b6537fcb04e3c6a4e56db9d883c06682e2e189a1b2234c412a224936fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee2879aa877fd3fc5831fc029db676d66d3e506782f7f836964f6b7b70dbbe2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d17eac27b3fcd0ccc656c80d3b5611487691fa4010b7bd570558181bcc774`  
		Last Modified: Tue, 04 Nov 2025 18:28:41 GMT  
		Size: 2.3 MB (2285009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327e0a83092a2b5e6b90c9f10c9f4cfd2fa1541fbcd2bbaa1a46c3b6057c9f1d`  
		Last Modified: Tue, 04 Nov 2025 18:28:42 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:1ad8ae3e827a63e119717cbc995ba416165edf47f802f35d9ec3a28b90874351
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
$ docker pull fluentd@sha256:afa3a57d73c7c0768f7045af02ff38c7956371261c95b23e523e6496fbb180c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17383642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6b44e684e6309468eb956f3d4740cf12ccb8c434b97a188b29da64c20b70e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78331f707c6d9910019296ecb4ab44f9b26a450a37e504c48be8963ce9a043`  
		Last Modified: Wed, 08 Oct 2025 23:22:10 GMT  
		Size: 14.0 MB (13961663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba1f53d18cef4c44a0dbd3daafb62cf57107f7f532fa0f57ef1b22d0af51e7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50b040b930bc5d13e08cdd1df716af2d3ff029e5b6b134e3e2fe71fad714b7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22932eecf8769ce42b56b0bc4a4f283b4d97f1f07d7f98efacbd1a1357ee27cd`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1769926942992a983f31805ed3a13d0406f50533e68b3d4d3236fa5963c45d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.2 KB (986159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53218b2014f588519fb6edb485d5b9268070ae8f517d0500d83a0f5a95462041`

```dockerfile
```

-	Layers:
	-	`sha256:3026734faa929ea6d5e52a4a4265ccb061d0836149b6fc9ef2bb6c9c7c6865c8`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 972.5 KB (972483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3dbf40f2c01bb6ecdda2f44a969772b89c46c3166fe5663350921ae5985e8e`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 13.7 KB (13676 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:46ac9bed32c7a8ce49660a59a52f753eff30538835dd611d22bc1f7934b37c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16137396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f885d67ca4b1bd990fa3007f4cfafb8bf90d6e39ff2be76552973966350f4fef`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-armhf.tar.gz / # buildkit
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
	-	`sha256:93e88a4aad08082395ce41ebaca8e4678e1148db5e8947e4c39599181a9ee4ba`  
		Last Modified: Wed, 08 Oct 2025 21:25:16 GMT  
		Size: 3.2 MB (3176528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf77ba4c6a48f3bacaaf9db6e676cc51c8898bc17f98b43aa29c349ccd9250`  
		Last Modified: Wed, 08 Oct 2025 22:39:21 GMT  
		Size: 13.0 MB (12958702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e42f64ef5aafe9d9b3ab4319844beb84a50b007d02d84fa103521d60f2f76`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c473ad81afc625e1af60d0c4ebf7c05152d7ea626b9f0c7875590101fae33`  
		Last Modified: Wed, 08 Oct 2025 22:39:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a4607d2da40a11eda63339c19317510928a2f1581ea6f29a6b9c0fe011d0c`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b1047a7ef72278952bd72515b06df4c47777ce18d0446c239adb2f9bdbe2e14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42935ff90a0ef9a2f68edaf9040d29def17f626d3c04096f9c92178845c3629d`

```dockerfile
```

-	Layers:
	-	`sha256:8015c3aa7387514211e92d6eee02a313c10bc707bafd172c2fd61a50d1311754`  
		Last Modified: Wed, 08 Oct 2025 23:28:29 GMT  
		Size: 13.5 KB (13539 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cef7f445d8c75f71a73b9c9ad0332a2c194fe935d3058f588c8dec4155186ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff98b6fa62f0c15cb2289ed831b50b438d943fc9324f96ee47ec3bff51bed3f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
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
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeb91e752132813c432d89f1a8dd1db5120bd0a105f5482c692c4c90eae17b3`  
		Last Modified: Wed, 08 Oct 2025 22:11:12 GMT  
		Size: 14.0 MB (14007447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df20c8f62a7ff47af002767397639763517b507053d3be2a607ad7cf039699cb`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8b09660f0729b33efa9eee73345d6e2574e683cff98f8189145136dd26dc4`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44991f0a648880052ce599ae6dc1fbcfeeea9db841398e692d720adc561c80c6`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bae4897fe1e09f33a0cb1995e2844559c6203a2de785f07457545055b868b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.4 KB (986385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93150014baf1f5b57526e2c5af7aea24f24a1f05f7958a7233428da7651d9dd`

```dockerfile
```

-	Layers:
	-	`sha256:67aba2f8a082f4bcbaa1ad6fc530073640b1b7742fa155f2fb1f96d7658cede5`  
		Last Modified: Wed, 08 Oct 2025 23:28:32 GMT  
		Size: 972.6 KB (972613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3629a5d26b2d4d23396554cd8b33525330b75f331ee1a61a6aa7b7b2bef527`  
		Last Modified: Wed, 08 Oct 2025 23:28:33 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:6a013d0b1dbe71756026d1ef1f8f07abf0ac51ead8815af66109c1a01414e18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16345474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dbc71c5e074c89edb50509532f4fb4a01d3e9ff2595e95a5533b13db016c55`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86.tar.gz / # buildkit
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
	-	`sha256:29ed29d5a2d3bb6de33b2b4bc58a076a8bccb81beedbcc013e38338640c314cf`  
		Last Modified: Wed, 08 Oct 2025 12:04:10 GMT  
		Size: 3.3 MB (3254171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29c80768044ac9f47738f5ba63e8f540639a570074a5dd04bc400d0468ebb8`  
		Last Modified: Wed, 08 Oct 2025 21:46:08 GMT  
		Size: 13.1 MB (13089135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e224de4549cda25d841df269ce3e9b86cd0feb6ef1703b75cb32524bedafe1`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1061097b93842eedc8d7863fc0608dbd3490771b515873cc3329b5cdc8fcbd`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5a6e02037353ec4b014f170080310354e526bc797bfe200c2286eedaf6ae8`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:755dd01070d905860704626ff1d1155994b4bf042e5aab8aa38bca75857fc293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.9 KB (982887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc6d533e4a0d8a4e7117c42fd122fbdcec92426815b69d138847435a5f42c2d`

```dockerfile
```

-	Layers:
	-	`sha256:e17fbd8db09214885631e52c7f3ee862a494b742523bb8f6acb292439080f164`  
		Last Modified: Wed, 08 Oct 2025 23:28:36 GMT  
		Size: 969.2 KB (969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83c293b83d79cb70ba9c955cedb86fdc401f653cba99c68d22f9fa322bab621`  
		Last Modified: Wed, 08 Oct 2025 23:28:37 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:62eb94d5f8bab0352fe1bda6749f90795526e823846751875ed5078f2f8704b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16932429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b60459341330d9f4e3d27c417ba023f6fe3fb7b0846fda2d34e07b63e813c3c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-ppc64le.tar.gz / # buildkit
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
	-	`sha256:8615c7c09f59391eedf1644cf56164e9680a9e5f673fc84abf83944731c13b07`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.4 MB (3364466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd729167cc2a515dbbde613e7ae787652d091f0141bb5881d946a962a54a4b4`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 13.6 MB (13565797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae39192a12d7e6272184f7dcbe45d1241c964aafe748d27068d19340c408c9`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58128b57f286f34d4522f0e60a4be46c9fad0ee0dcf950dc879b1dcf511804ff`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63d13a8c0219e4550fb93a4d23eb5ecebf4f0cb4dbf998c38c7538a6243f718`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:23f4110435b3c619f0c6dfd9bc4b503e4d1f29f43cc89d63a31362be157e36aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.7 KB (981716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e38f607b22ca7f6244be9c7241bb070aeec1e5087b0cf13bf0ac887e0dde105`

```dockerfile
```

-	Layers:
	-	`sha256:ab9c1e7d5cf37454b207e160b91793faa0c78f73788b2c5eb29bd4c53c8b6970`  
		Last Modified: Thu, 09 Oct 2025 08:28:29 GMT  
		Size: 968.0 KB (968006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ccd55a5597ae933a84d99a7a7f1903f8379b62a381c32ab960f5b9cd3b64b58`  
		Last Modified: Thu, 09 Oct 2025 08:28:30 GMT  
		Size: 13.7 KB (13710 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:0b41672737621c0b4d9636f2680dc26702a455105378c6fddfde27ccd0dc7754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16767969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55cf05ab6ec22da0c19bd4f8545dddd8e4be8caddc43341112665a1915a7201`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-s390x.tar.gz / # buildkit
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
	-	`sha256:913efc36ec133ccc056e722147d93d8138aa999785d2ce858104b0c2d0e78fd6`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.3 MB (3253007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd32227ea6240b7d955081f56cf0e5cc573c44dd77407da8bb53c063ab87b71`  
		Last Modified: Thu, 09 Oct 2025 14:10:11 GMT  
		Size: 13.5 MB (13512798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fab613ee49849eb1192e5b5aca71cbeabae4d8c9ed4297bbc7070c859d579b3`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1655c318dd63d9aadb21ad09dc3762229e1cecd22e44d14c481db0c808efcc1`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed09bc671cc79a80b0e31f178bdf4318f525b2880e56c471dffebf3a859f886`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:48b41953e35001058187fa9db056f5f99dd35a109572db363ed221550ec063b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.1 KB (981071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab11aac5ad8d7f16b2e926d62908dbe2278ca45cffe6b3527a559b15741ff15`

```dockerfile
```

-	Layers:
	-	`sha256:370521b0c1295049f7e15fcdc00056580fd5959e7fb0423f9759e0b2cd663222`  
		Last Modified: Thu, 09 Oct 2025 14:28:31 GMT  
		Size: 967.4 KB (967396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129be691f47d14c09692973c170d7b9564fd1a2535581688d141759c73b4a009`  
		Last Modified: Thu, 09 Oct 2025 14:28:32 GMT  
		Size: 13.7 KB (13675 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:e2c7d9954a9eaf012e45931d1df763012c1a925c41dabaa67ca76c3fc50c9826
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
$ docker pull fluentd@sha256:b7b1505e2d71d581def93acb1c17449e50ce5490a9a9b735ceec1add91da9f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81976600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2866f2dcf474713b56789d63a1c62318e21f35bfa8efb05083150d4373b5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:44:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:44:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 00:49:43 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:49:43 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 00:49:43 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 00:49:43 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 00:49:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 00:49:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:49:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 00:49:43 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 04:35:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 04:35:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 04:35:41 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 04:35:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 04:35:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 04:35:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 04:35:41 GMT
USER fluent
# Tue, 04 Nov 2025 04:35:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f68f997c30e296d96f9b485f3f87fd66a41d1569bde05ea0addf8681f3cee5`  
		Last Modified: Tue, 04 Nov 2025 00:47:31 GMT  
		Size: 3.5 MB (3509713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc98f322558b85574da564d1a699700e1b86f30bb1232963ca4e5b50aa9e2c4`  
		Last Modified: Tue, 04 Nov 2025 00:47:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dec182ef9642198522a0ddc6e2f9618b89402b7feab139f7f7ccf27ad4847d8`  
		Last Modified: Tue, 04 Nov 2025 00:49:59 GMT  
		Size: 36.0 MB (35964222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d60492d38d7fa1d3403dffc56be6a2929fb218d8e5ecf821701a83e9f58679f`  
		Last Modified: Tue, 04 Nov 2025 00:49:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c018157f787eb093f4bd3b73ac94283b028497f550609f3913148d7197e90c68`  
		Last Modified: Tue, 04 Nov 2025 04:35:58 GMT  
		Size: 14.3 MB (14271707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8e44967ec0c6728474869540f9c0998cc8769bcd8c9213cb474459c7253b2c`  
		Last Modified: Tue, 04 Nov 2025 04:35:56 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6af0ec48295a26501c9e29c8d4e4d6791881aebbdcf5d54433d9a1d44be421`  
		Last Modified: Tue, 04 Nov 2025 04:35:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe1f471d7bbc65c8e38ee11fd644ab157d0c7dbb0120782c93aca95489a243e`  
		Last Modified: Tue, 04 Nov 2025 04:35:56 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:346812909d7861d823ae92b7c0ca223df21ce9d3a042a674f35366577762a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6be24856589d37d358ffcbeb9e6a0fe6e71ba15a45c230252d32de879c56d58`

```dockerfile
```

-	Layers:
	-	`sha256:f5fcbb6fcf499e0eec532336b806aacf83c2e88a94000115deb007f60ac4dc52`  
		Last Modified: Tue, 04 Nov 2025 09:28:44 GMT  
		Size: 2.7 MB (2668452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e894701430c39ca6a47ad370fa529d5aaa2d5cbb814051d3597361ceeddfbd9`  
		Last Modified: Tue, 04 Nov 2025 09:28:45 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:15b64e0fd4162ae5d056943a22573ca147389050286521bbe2f4d760d17567e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cbac93bc99cc5fdfab88c444893f98ff5d71a0fb527121625c23a624161031`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:34:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:34:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:34:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:34:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:34:04 GMT
USER fluent
# Tue, 18 Nov 2025 05:34:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:34:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76389c7791ac539e08f00ada6c0d8e63fb2875388ac5be539590ff77fa593d6`  
		Last Modified: Tue, 18 Nov 2025 04:21:40 GMT  
		Size: 3.1 MB (3079850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58dfc7ad8f3d981491eff3548b814629f9594b76173cfba1b38d23839061a86`  
		Last Modified: Tue, 18 Nov 2025 04:21:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a479b7ac057a0f4485088567a448a9324d019e266525d79d0b4dd8b9968fa8`  
		Last Modified: Tue, 18 Nov 2025 04:24:45 GMT  
		Size: 32.3 MB (32327214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450839ed4674e7308e9f7f985d309da887b11fd14e92704dab4f77a6ebc15e9e`  
		Last Modified: Tue, 18 Nov 2025 04:24:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0fd05fee9eeae456f90dbd571124d2ad5a2240e039f2dc9f6b4ebc2140d9c5`  
		Last Modified: Tue, 18 Nov 2025 05:34:20 GMT  
		Size: 14.3 MB (14252439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3beb25103dd976dfe482fdb173eb9929e23f669a1812b8fc47bb715ecd459cf`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac208bcd85cb9a2d2e3dcc6d4329be633f2d58ff9524ae4a6a531e7a5c8cea`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa35afe7bbfb4076da474085792f28f9581cd063df1c5d35686fc9e874fb75d`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:463d6110b7a9c0727e420b063e6ad8bc7225cd82894c89c1edacca6e6aab85a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d823bc78b2159cc078821e7fba871cfad90af83c4d41aa1457662f6606abc4d`

```dockerfile
```

-	Layers:
	-	`sha256:6957e480a4692006176772042905e24d6bb195f08da82aaf9b707fee590dfd51`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 2.7 MB (2672247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbc786027331eb6d2974efb5ebeb9a98b3f82c15369e282681c82a4298a93db`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:2d1371bbb11c44359f6246f282009a94f9af5bab5f607d90dd7ad4ddde19e9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73190376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a518e5642cc9073f3be290e8de97233b78fd27db65b092777c8f5fed4e51665e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:24:57 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:24:57 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 01:24:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 01:24:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 01:24:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:24:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:24:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:24:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:24:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:24:57 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:07:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:07:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 03:07:51 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 03:07:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:07:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:07:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:07:51 GMT
USER fluent
# Tue, 04 Nov 2025 03:07:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:07:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a40ec974c0fda9ca1c4f47f178d382b3b04a0e2c0c174d2d616eb786d76d086`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 2.9 MB (2912766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095856f2d904d2da335efc38ab1e713515b102d50b37f162147533a4971807a`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd19123dd286279c32b91bbd297cf4d6acceb44c8da64ae9e1360174870d31`  
		Last Modified: Tue, 04 Nov 2025 01:25:16 GMT  
		Size: 32.2 MB (32161909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f50778beadd71bddcafa252c3f2246635cb797518c3e7b3500733a05531f0`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82299ec51c45d89aa4aa1a0838e67a0cc825230ac30b0290c1e9d87567318266`  
		Last Modified: Tue, 04 Nov 2025 03:08:08 GMT  
		Size: 14.2 MB (14179188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ead8fdd335aa00ade79105aabd7885bddb77aabbf506fb96304db3c15fca770`  
		Last Modified: Tue, 04 Nov 2025 03:08:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47142b9438b9838ed6cba2ae203110cdc2f8bc4477b75b401fa9d1ce222c161`  
		Last Modified: Tue, 04 Nov 2025 03:08:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67fcfd8fcd153b4ed47ab7e0abf50015de2e8e78afd32efe39df04e3c6be3c0`  
		Last Modified: Tue, 04 Nov 2025 03:08:07 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6e50a97175fc15653f3716bf5e0069060046d9156887321100ed46504b26f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b159d4973a9c7aa9415e587d48668322ee71fdcd8e4f4eb2a3f3bf4de3795`

```dockerfile
```

-	Layers:
	-	`sha256:cd303b7e6869ce189f4bb2e64276bca8f054e2c7db5996fdd4968e6634127fe9`  
		Last Modified: Tue, 04 Nov 2025 12:28:42 GMT  
		Size: 2.7 MB (2670678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d6fd9310c7e66f30a7ba0c380f7120eebd9bddc8954c3331a6ac84e37f7b8f`  
		Last Modified: Tue, 04 Nov 2025 12:28:43 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:e4adbc03b222b4c68855d4ee1f96d0b992308786ddb56edb084b88509cc71082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81625897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c625c6a2ff15b8fa5f39304719292233d4182c4da0eaaba3db545a9411241816`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:46:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 00:49:08 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:49:08 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 00:49:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 00:49:08 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 00:49:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 00:49:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:49:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 00:49:08 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 01:50:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 01:50:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 01:50:37 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 01:50:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 01:50:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 01:50:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 01:50:37 GMT
USER fluent
# Tue, 04 Nov 2025 01:50:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3823f037b70c41ecc00a6f2d0b2fc7263b297058c445125961e26de8d7c135e`  
		Last Modified: Tue, 04 Nov 2025 00:49:26 GMT  
		Size: 3.3 MB (3340651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1dcbe472a4cca517cbccfe184a251cefd7ea2fb2da816f093f160c41459d44`  
		Last Modified: Tue, 04 Nov 2025 00:49:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008555cb6452b9452f147f6d1ad2bf84b8c481b20faef205092ec5e24e00a25`  
		Last Modified: Tue, 04 Nov 2025 00:49:31 GMT  
		Size: 35.9 MB (35900683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b367beaf9ba47acfcfc3e846f7f9ccbd42d39e8852aa84b2af263c04d5295e1d`  
		Last Modified: Tue, 04 Nov 2025 00:49:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faa3d68d3a0b14aacf7c5570bed6dfb57ff38379784b07fd88cf8a833c9bcb2`  
		Last Modified: Tue, 04 Nov 2025 01:50:50 GMT  
		Size: 14.3 MB (14279802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e41a4701bd60b9bec299db3a3adf87d11622c82d15bca509ab94650efc0bbe3`  
		Last Modified: Tue, 04 Nov 2025 01:50:50 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97600259c6fd4b1eae341aac6d964e2eb9162e9a08f93d4751eb8a1b8f89ee38`  
		Last Modified: Tue, 04 Nov 2025 01:50:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8cf4bcb6880345f8f199a06190bc2e998b75a9dbd7370098094fc614d15358`  
		Last Modified: Tue, 04 Nov 2025 01:50:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5a10aecbde71e7cb9b49529bdc27967eb1beb10b450df81d980767e20252256b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f545406e00fdad723a3768058d6a3f51b60dc54c2fc44a95782dd618ab529d1`

```dockerfile
```

-	Layers:
	-	`sha256:b21d6a059cf580534938c8239845abe581fe6f59e1feedf02ea5228d2c28ee70`  
		Last Modified: Tue, 04 Nov 2025 12:28:47 GMT  
		Size: 2.7 MB (2668692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec52797ff3d9bf09e72847fa82e8fb6e0edbe9010a30abdeb39cb19e1abee9d`  
		Last Modified: Tue, 04 Nov 2025 12:28:47 GMT  
		Size: 21.2 KB (21156 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5df4e8b2e830a5003333e290ce271796fdfc7bf162a3fa4a7128ed51cfef0686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23bc26f4db07b606df02f14ce3b529bd3b232e9d0dc8e86d66bebd934352301`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:22:34 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:22:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:22:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:22:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:22:34 GMT
USER fluent
# Tue, 18 Nov 2025 05:22:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:22:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ae260a61c110779bd438deac4d1cd76065ff2394ea83afc9ff5529ea91071`  
		Last Modified: Tue, 18 Nov 2025 03:42:47 GMT  
		Size: 3.5 MB (3510984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356fe9a31a02a164458a68e3f079e86eabe6530bc2f61ae1772c93ea96dfa2a`  
		Last Modified: Tue, 18 Nov 2025 03:42:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0b280db48ee6f86ec56584743697a062ecc6953d4df02a3fe330846b9913a`  
		Last Modified: Tue, 18 Nov 2025 03:46:03 GMT  
		Size: 32.2 MB (32160063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23894894335470a52957a4ef6504faf802a94d333679fd77a4c50a500ae296d0`  
		Last Modified: Tue, 18 Nov 2025 03:46:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979287a7b7479f4b091297b8dde77dd57c16255c1122c316d64dc56986cbe84a`  
		Last Modified: Tue, 18 Nov 2025 05:22:51 GMT  
		Size: 14.1 MB (14066199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daafd6d338e29911ba2ed0bb0dc4f03149fa5d57f96910e6062ca814f1d2cb`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a19ba85eb93000ad493ae17988dc6f1cebc1b849fe17484acbca51ea4e25ea`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757e96ba36c6bae804639ca2dadf2349a78d93393529d6377d411a1e46eb13e2`  
		Last Modified: Tue, 18 Nov 2025 05:22:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3e0f8b5b437688f58383aa7bbf12ccce82a250f7adc1aaea24df67d02376cd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97badbe75c72a0883ff7fa244c548058584d26342bdbe2a1a40dd9da77026744`

```dockerfile
```

-	Layers:
	-	`sha256:9c8cce8e3dfe4cce97ae219a474956647bbc2d50d4f9c0348172ec67f4c23f8b`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 2.7 MB (2665631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcee889ac2455f6b2a0a490ac2e27e5e15a2c2abafd1f3913fbfb7a83acea5f`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:a38d80ee2741c444bb4d78eec39c472e7142555a187977719b810e56737eaa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84284683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c1025723ca160e4657f60b6f4a0af2a0e357eaf312ec7a43e3044990f804da`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 12:21:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 12:21:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:52:48 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:52:48 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 12:52:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 12:52:48 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 12:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:52:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:52:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:52:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:52:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:52:49 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:52:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:52:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 19:52:43 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 19:52:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:52:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:52:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:52:44 GMT
USER fluent
# Tue, 04 Nov 2025 19:52:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:52:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8143fbf0f893350a0d0f8d7e79c8f5671506d0e0a728c087e659b8953f7c93e4`  
		Last Modified: Tue, 04 Nov 2025 12:25:39 GMT  
		Size: 3.7 MB (3709076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b9de7bb388d880720eef9fc2101448ebf22fa5da782c4633dc51c9571b3fa`  
		Last Modified: Tue, 04 Nov 2025 12:25:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326d61f4903134b5057582473b8ba1ad2092eb821b96d773d749a73fce65bcb6`  
		Last Modified: Tue, 04 Nov 2025 12:53:30 GMT  
		Size: 33.8 MB (33832724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2c39c8617763720d792c9cdba652f68a35fd74e12df5f03d24fe74ce1209`  
		Last Modified: Tue, 04 Nov 2025 12:53:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a7798e76604a4dd7505fd04cbb6218980d9b6d02ad79ec9e987a8bdb973b5`  
		Last Modified: Tue, 04 Nov 2025 19:53:31 GMT  
		Size: 14.7 MB (14671591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4a87ab8faffe3819a8b2c92392409d8a8b687a425c3c81a19767f21dd680f`  
		Last Modified: Tue, 04 Nov 2025 19:53:29 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59960f93e0d6e004964b590a19fce8832fbcd20804ee0112b8631c36d41008a9`  
		Last Modified: Tue, 04 Nov 2025 19:53:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5f4b0401b5e9251cf47c9fb6e6289c3eb03a62abbf604d19527979d60e266c`  
		Last Modified: Tue, 04 Nov 2025 19:53:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3dbffe8c2c68790680a1b3fd2d1cc26b9e420ab4b14bfd93d4616aa030f808dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef226def38f94add13edbc27c0ba7b4732b1ff1269959b7539aafc20560b31ff`

```dockerfile
```

-	Layers:
	-	`sha256:28104fbc29223a553ad8b546b3f4b3743b108952f858a7412f2c2e0e2e586fb5`  
		Last Modified: Tue, 04 Nov 2025 21:28:43 GMT  
		Size: 2.7 MB (2672869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8560342a4a2268ae1a24a54c0b2046e25ff5763a87f2cb8c0b9bf892f31939ec`  
		Last Modified: Tue, 04 Nov 2025 21:28:44 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:5992a68f45d51d6f99314b75f2bb91c3ace61db1a745b1c2900cc4cf1ec9bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bfeed593c818f2c455874423d250b6b14382e85d23431a94b18fc5b1abcc93`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:02:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 06:13:39 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:13:39 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 06:13:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 06:13:39 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 06:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 06:13:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 06:13:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 06:13:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:13:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 06:13:39 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:49:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:49:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 16:49:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 16:49:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:49:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:49:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:49:36 GMT
USER fluent
# Tue, 04 Nov 2025 16:49:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:49:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2508423c296a194164ad7e8012377ae140ab815233294177a81d624e5b13a37f`  
		Last Modified: Tue, 04 Nov 2025 06:04:55 GMT  
		Size: 3.2 MB (3170294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2434e8e8caf77576c0fe5d3fae1e9e026b80c16b8591fd2d5c34c60b2f7357b`  
		Last Modified: Tue, 04 Nov 2025 06:04:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619f8637cfe20a673bd0eed22af0c0ebed0146411e746709a6dfa9286eed16b6`  
		Last Modified: Tue, 04 Nov 2025 06:14:03 GMT  
		Size: 33.1 MB (33099333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1f7b8806e6bb69ec6303f9e1cf2741a10643fab10adbfecc7911cdd8c42cff`  
		Last Modified: Tue, 04 Nov 2025 06:14:01 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37497bcdd36e54fec25e6ad5e250014e87d26ff144feba42000fd8fd47673533`  
		Last Modified: Tue, 04 Nov 2025 16:50:01 GMT  
		Size: 14.4 MB (14408192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e4ddcd3465e4c02dc022bbc8fc6138a9c64a4e186bbe8d0765dec43b1ed73f`  
		Last Modified: Tue, 04 Nov 2025 16:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace6271687afe97f2c9d39256c9973c2f6dbc78dffeab237ea67484cacf29d30`  
		Last Modified: Tue, 04 Nov 2025 16:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3fc37ab0266a9acd2af0ca50d0df899e270162904a34503a1722fc954336e8`  
		Last Modified: Tue, 04 Nov 2025 16:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b6a6af06f63b7889d10a7125c144af5109914a5d108af5c7a218a8945afc05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b99451d889163960c9765b4b1468d70ad3e9b262d1ba651a43de32e813e8095`

```dockerfile
```

-	Layers:
	-	`sha256:c262a5feb2433c116c299777c925191d9b9fcf4b364ebbc302ca58e976ce7475`  
		Last Modified: Tue, 04 Nov 2025 18:28:51 GMT  
		Size: 2.7 MB (2665277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22cd35899d433493177bf4e9297bdacb223f97baa39141c96bc04576cb64520a`  
		Last Modified: Tue, 04 Nov 2025 18:28:52 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.9-1.0`

```console
$ docker pull fluentd@sha256:1ad8ae3e827a63e119717cbc995ba416165edf47f802f35d9ec3a28b90874351
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
$ docker pull fluentd@sha256:afa3a57d73c7c0768f7045af02ff38c7956371261c95b23e523e6496fbb180c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17383642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6b44e684e6309468eb956f3d4740cf12ccb8c434b97a188b29da64c20b70e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78331f707c6d9910019296ecb4ab44f9b26a450a37e504c48be8963ce9a043`  
		Last Modified: Wed, 08 Oct 2025 23:22:10 GMT  
		Size: 14.0 MB (13961663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba1f53d18cef4c44a0dbd3daafb62cf57107f7f532fa0f57ef1b22d0af51e7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50b040b930bc5d13e08cdd1df716af2d3ff029e5b6b134e3e2fe71fad714b7`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22932eecf8769ce42b56b0bc4a4f283b4d97f1f07d7f98efacbd1a1357ee27cd`  
		Last Modified: Wed, 08 Oct 2025 23:22:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1769926942992a983f31805ed3a13d0406f50533e68b3d4d3236fa5963c45d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.2 KB (986159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53218b2014f588519fb6edb485d5b9268070ae8f517d0500d83a0f5a95462041`

```dockerfile
```

-	Layers:
	-	`sha256:3026734faa929ea6d5e52a4a4265ccb061d0836149b6fc9ef2bb6c9c7c6865c8`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 972.5 KB (972483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3dbf40f2c01bb6ecdda2f44a969772b89c46c3166fe5663350921ae5985e8e`  
		Last Modified: Thu, 09 Oct 2025 02:28:21 GMT  
		Size: 13.7 KB (13676 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:46ac9bed32c7a8ce49660a59a52f753eff30538835dd611d22bc1f7934b37c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16137396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f885d67ca4b1bd990fa3007f4cfafb8bf90d6e39ff2be76552973966350f4fef`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-armhf.tar.gz / # buildkit
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
	-	`sha256:93e88a4aad08082395ce41ebaca8e4678e1148db5e8947e4c39599181a9ee4ba`  
		Last Modified: Wed, 08 Oct 2025 21:25:16 GMT  
		Size: 3.2 MB (3176528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf77ba4c6a48f3bacaaf9db6e676cc51c8898bc17f98b43aa29c349ccd9250`  
		Last Modified: Wed, 08 Oct 2025 22:39:21 GMT  
		Size: 13.0 MB (12958702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e42f64ef5aafe9d9b3ab4319844beb84a50b007d02d84fa103521d60f2f76`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c473ad81afc625e1af60d0c4ebf7c05152d7ea626b9f0c7875590101fae33`  
		Last Modified: Wed, 08 Oct 2025 22:39:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a4607d2da40a11eda63339c19317510928a2f1581ea6f29a6b9c0fe011d0c`  
		Last Modified: Wed, 08 Oct 2025 22:39:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b1047a7ef72278952bd72515b06df4c47777ce18d0446c239adb2f9bdbe2e14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42935ff90a0ef9a2f68edaf9040d29def17f626d3c04096f9c92178845c3629d`

```dockerfile
```

-	Layers:
	-	`sha256:8015c3aa7387514211e92d6eee02a313c10bc707bafd172c2fd61a50d1311754`  
		Last Modified: Wed, 08 Oct 2025 23:28:29 GMT  
		Size: 13.5 KB (13539 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cef7f445d8c75f71a73b9c9ad0332a2c194fe935d3058f588c8dec4155186ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff98b6fa62f0c15cb2289ed831b50b438d943fc9324f96ee47ec3bff51bed3f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
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
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeb91e752132813c432d89f1a8dd1db5120bd0a105f5482c692c4c90eae17b3`  
		Last Modified: Wed, 08 Oct 2025 22:11:12 GMT  
		Size: 14.0 MB (14007447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df20c8f62a7ff47af002767397639763517b507053d3be2a607ad7cf039699cb`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8b09660f0729b33efa9eee73345d6e2574e683cff98f8189145136dd26dc4`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44991f0a648880052ce599ae6dc1fbcfeeea9db841398e692d720adc561c80c6`  
		Last Modified: Wed, 08 Oct 2025 22:11:11 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bae4897fe1e09f33a0cb1995e2844559c6203a2de785f07457545055b868b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.4 KB (986385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93150014baf1f5b57526e2c5af7aea24f24a1f05f7958a7233428da7651d9dd`

```dockerfile
```

-	Layers:
	-	`sha256:67aba2f8a082f4bcbaa1ad6fc530073640b1b7742fa155f2fb1f96d7658cede5`  
		Last Modified: Wed, 08 Oct 2025 23:28:32 GMT  
		Size: 972.6 KB (972613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3629a5d26b2d4d23396554cd8b33525330b75f331ee1a61a6aa7b7b2bef527`  
		Last Modified: Wed, 08 Oct 2025 23:28:33 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:6a013d0b1dbe71756026d1ef1f8f07abf0ac51ead8815af66109c1a01414e18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16345474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dbc71c5e074c89edb50509532f4fb4a01d3e9ff2595e95a5533b13db016c55`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-x86.tar.gz / # buildkit
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
	-	`sha256:29ed29d5a2d3bb6de33b2b4bc58a076a8bccb81beedbcc013e38338640c314cf`  
		Last Modified: Wed, 08 Oct 2025 12:04:10 GMT  
		Size: 3.3 MB (3254171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29c80768044ac9f47738f5ba63e8f540639a570074a5dd04bc400d0468ebb8`  
		Last Modified: Wed, 08 Oct 2025 21:46:08 GMT  
		Size: 13.1 MB (13089135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e224de4549cda25d841df269ce3e9b86cd0feb6ef1703b75cb32524bedafe1`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1061097b93842eedc8d7863fc0608dbd3490771b515873cc3329b5cdc8fcbd`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5a6e02037353ec4b014f170080310354e526bc797bfe200c2286eedaf6ae8`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:755dd01070d905860704626ff1d1155994b4bf042e5aab8aa38bca75857fc293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.9 KB (982887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc6d533e4a0d8a4e7117c42fd122fbdcec92426815b69d138847435a5f42c2d`

```dockerfile
```

-	Layers:
	-	`sha256:e17fbd8db09214885631e52c7f3ee862a494b742523bb8f6acb292439080f164`  
		Last Modified: Wed, 08 Oct 2025 23:28:36 GMT  
		Size: 969.2 KB (969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83c293b83d79cb70ba9c955cedb86fdc401f653cba99c68d22f9fa322bab621`  
		Last Modified: Wed, 08 Oct 2025 23:28:37 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:62eb94d5f8bab0352fe1bda6749f90795526e823846751875ed5078f2f8704b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16932429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b60459341330d9f4e3d27c417ba023f6fe3fb7b0846fda2d34e07b63e813c3c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-ppc64le.tar.gz / # buildkit
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
	-	`sha256:8615c7c09f59391eedf1644cf56164e9680a9e5f673fc84abf83944731c13b07`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.4 MB (3364466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd729167cc2a515dbbde613e7ae787652d091f0141bb5881d946a962a54a4b4`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 13.6 MB (13565797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae39192a12d7e6272184f7dcbe45d1241c964aafe748d27068d19340c408c9`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58128b57f286f34d4522f0e60a4be46c9fad0ee0dcf950dc879b1dcf511804ff`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63d13a8c0219e4550fb93a4d23eb5ecebf4f0cb4dbf998c38c7538a6243f718`  
		Last Modified: Thu, 09 Oct 2025 05:16:07 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:23f4110435b3c619f0c6dfd9bc4b503e4d1f29f43cc89d63a31362be157e36aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.7 KB (981716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e38f607b22ca7f6244be9c7241bb070aeec1e5087b0cf13bf0ac887e0dde105`

```dockerfile
```

-	Layers:
	-	`sha256:ab9c1e7d5cf37454b207e160b91793faa0c78f73788b2c5eb29bd4c53c8b6970`  
		Last Modified: Thu, 09 Oct 2025 08:28:29 GMT  
		Size: 968.0 KB (968006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ccd55a5597ae933a84d99a7a7f1903f8379b62a381c32ab960f5b9cd3b64b58`  
		Last Modified: Thu, 09 Oct 2025 08:28:30 GMT  
		Size: 13.7 KB (13710 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:0b41672737621c0b4d9636f2680dc26702a455105378c6fddfde27ccd0dc7754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16767969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55cf05ab6ec22da0c19bd4f8545dddd8e4be8caddc43341112665a1915a7201`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.9-s390x.tar.gz / # buildkit
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
	-	`sha256:913efc36ec133ccc056e722147d93d8138aa999785d2ce858104b0c2d0e78fd6`  
		Last Modified: Wed, 08 Oct 2025 12:04:09 GMT  
		Size: 3.3 MB (3253007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd32227ea6240b7d955081f56cf0e5cc573c44dd77407da8bb53c063ab87b71`  
		Last Modified: Thu, 09 Oct 2025 14:10:11 GMT  
		Size: 13.5 MB (13512798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fab613ee49849eb1192e5b5aca71cbeabae4d8c9ed4297bbc7070c859d579b3`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1655c318dd63d9aadb21ad09dc3762229e1cecd22e44d14c481db0c808efcc1`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed09bc671cc79a80b0e31f178bdf4318f525b2880e56c471dffebf3a859f886`  
		Last Modified: Thu, 09 Oct 2025 14:10:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:48b41953e35001058187fa9db056f5f99dd35a109572db363ed221550ec063b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.1 KB (981071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab11aac5ad8d7f16b2e926d62908dbe2278ca45cffe6b3527a559b15741ff15`

```dockerfile
```

-	Layers:
	-	`sha256:370521b0c1295049f7e15fcdc00056580fd5959e7fb0423f9759e0b2cd663222`  
		Last Modified: Thu, 09 Oct 2025 14:28:31 GMT  
		Size: 967.4 KB (967396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129be691f47d14c09692973c170d7b9564fd1a2535581688d141759c73b4a009`  
		Last Modified: Thu, 09 Oct 2025 14:28:32 GMT  
		Size: 13.7 KB (13675 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.9-debian-1.0`

```console
$ docker pull fluentd@sha256:e2c7d9954a9eaf012e45931d1df763012c1a925c41dabaa67ca76c3fc50c9826
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
$ docker pull fluentd@sha256:b7b1505e2d71d581def93acb1c17449e50ce5490a9a9b735ceec1add91da9f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81976600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2866f2dcf474713b56789d63a1c62318e21f35bfa8efb05083150d4373b5c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:44:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:44:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 00:49:43 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:49:43 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 00:49:43 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 00:49:43 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 00:49:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 00:49:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:49:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 00:49:43 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 04:35:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 04:35:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 04:35:41 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 04:35:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 04:35:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 04:35:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 04:35:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 04:35:41 GMT
USER fluent
# Tue, 04 Nov 2025 04:35:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f68f997c30e296d96f9b485f3f87fd66a41d1569bde05ea0addf8681f3cee5`  
		Last Modified: Tue, 04 Nov 2025 00:47:31 GMT  
		Size: 3.5 MB (3509713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc98f322558b85574da564d1a699700e1b86f30bb1232963ca4e5b50aa9e2c4`  
		Last Modified: Tue, 04 Nov 2025 00:47:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dec182ef9642198522a0ddc6e2f9618b89402b7feab139f7f7ccf27ad4847d8`  
		Last Modified: Tue, 04 Nov 2025 00:49:59 GMT  
		Size: 36.0 MB (35964222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d60492d38d7fa1d3403dffc56be6a2929fb218d8e5ecf821701a83e9f58679f`  
		Last Modified: Tue, 04 Nov 2025 00:49:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c018157f787eb093f4bd3b73ac94283b028497f550609f3913148d7197e90c68`  
		Last Modified: Tue, 04 Nov 2025 04:35:58 GMT  
		Size: 14.3 MB (14271707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8e44967ec0c6728474869540f9c0998cc8769bcd8c9213cb474459c7253b2c`  
		Last Modified: Tue, 04 Nov 2025 04:35:56 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6af0ec48295a26501c9e29c8d4e4d6791881aebbdcf5d54433d9a1d44be421`  
		Last Modified: Tue, 04 Nov 2025 04:35:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe1f471d7bbc65c8e38ee11fd644ab157d0c7dbb0120782c93aca95489a243e`  
		Last Modified: Tue, 04 Nov 2025 04:35:56 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:346812909d7861d823ae92b7c0ca223df21ce9d3a042a674f35366577762a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6be24856589d37d358ffcbeb9e6a0fe6e71ba15a45c230252d32de879c56d58`

```dockerfile
```

-	Layers:
	-	`sha256:f5fcbb6fcf499e0eec532336b806aacf83c2e88a94000115deb007f60ac4dc52`  
		Last Modified: Tue, 04 Nov 2025 09:28:44 GMT  
		Size: 2.7 MB (2668452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e894701430c39ca6a47ad370fa529d5aaa2d5cbb814051d3597361ceeddfbd9`  
		Last Modified: Tue, 04 Nov 2025 09:28:45 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:15b64e0fd4162ae5d056943a22573ca147389050286521bbe2f4d760d17567e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75419428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cbac93bc99cc5fdfab88c444893f98ff5d71a0fb527121625c23a624161031`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:24:28 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:24:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:24:28 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:34:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:34:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:34:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:34:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:34:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:34:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:34:04 GMT
USER fluent
# Tue, 18 Nov 2025 05:34:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:34:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76389c7791ac539e08f00ada6c0d8e63fb2875388ac5be539590ff77fa593d6`  
		Last Modified: Tue, 18 Nov 2025 04:21:40 GMT  
		Size: 3.1 MB (3079850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58dfc7ad8f3d981491eff3548b814629f9594b76173cfba1b38d23839061a86`  
		Last Modified: Tue, 18 Nov 2025 04:21:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a479b7ac057a0f4485088567a448a9324d019e266525d79d0b4dd8b9968fa8`  
		Last Modified: Tue, 18 Nov 2025 04:24:45 GMT  
		Size: 32.3 MB (32327214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450839ed4674e7308e9f7f985d309da887b11fd14e92704dab4f77a6ebc15e9e`  
		Last Modified: Tue, 18 Nov 2025 04:24:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0fd05fee9eeae456f90dbd571124d2ad5a2240e039f2dc9f6b4ebc2140d9c5`  
		Last Modified: Tue, 18 Nov 2025 05:34:20 GMT  
		Size: 14.3 MB (14252439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3beb25103dd976dfe482fdb173eb9929e23f669a1812b8fc47bb715ecd459cf`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac208bcd85cb9a2d2e3dcc6d4329be633f2d58ff9524ae4a6a531e7a5c8cea`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa35afe7bbfb4076da474085792f28f9581cd063df1c5d35686fc9e874fb75d`  
		Last Modified: Tue, 18 Nov 2025 05:34:18 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:463d6110b7a9c0727e420b063e6ad8bc7225cd82894c89c1edacca6e6aab85a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d823bc78b2159cc078821e7fba871cfad90af83c4d41aa1457662f6606abc4d`

```dockerfile
```

-	Layers:
	-	`sha256:6957e480a4692006176772042905e24d6bb195f08da82aaf9b707fee590dfd51`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 2.7 MB (2672247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbc786027331eb6d2974efb5ebeb9a98b3f82c15369e282681c82a4298a93db`  
		Last Modified: Tue, 18 Nov 2025 06:32:11 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:2d1371bbb11c44359f6246f282009a94f9af5bab5f607d90dd7ad4ddde19e9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73190376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a518e5642cc9073f3be290e8de97233b78fd27db65b092777c8f5fed4e51665e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:24:57 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:24:57 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 01:24:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 01:24:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 01:24:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:24:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:24:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:24:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:24:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:24:57 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:07:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:07:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 03:07:51 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 03:07:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:07:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:07:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:07:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:07:51 GMT
USER fluent
# Tue, 04 Nov 2025 03:07:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:07:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a40ec974c0fda9ca1c4f47f178d382b3b04a0e2c0c174d2d616eb786d76d086`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 2.9 MB (2912766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095856f2d904d2da335efc38ab1e713515b102d50b37f162147533a4971807a`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fd19123dd286279c32b91bbd297cf4d6acceb44c8da64ae9e1360174870d31`  
		Last Modified: Tue, 04 Nov 2025 01:25:16 GMT  
		Size: 32.2 MB (32161909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f50778beadd71bddcafa252c3f2246635cb797518c3e7b3500733a05531f0`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82299ec51c45d89aa4aa1a0838e67a0cc825230ac30b0290c1e9d87567318266`  
		Last Modified: Tue, 04 Nov 2025 03:08:08 GMT  
		Size: 14.2 MB (14179188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ead8fdd335aa00ade79105aabd7885bddb77aabbf506fb96304db3c15fca770`  
		Last Modified: Tue, 04 Nov 2025 03:08:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47142b9438b9838ed6cba2ae203110cdc2f8bc4477b75b401fa9d1ce222c161`  
		Last Modified: Tue, 04 Nov 2025 03:08:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67fcfd8fcd153b4ed47ab7e0abf50015de2e8e78afd32efe39df04e3c6be3c0`  
		Last Modified: Tue, 04 Nov 2025 03:08:07 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6e50a97175fc15653f3716bf5e0069060046d9156887321100ed46504b26f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b159d4973a9c7aa9415e587d48668322ee71fdcd8e4f4eb2a3f3bf4de3795`

```dockerfile
```

-	Layers:
	-	`sha256:cd303b7e6869ce189f4bb2e64276bca8f054e2c7db5996fdd4968e6634127fe9`  
		Last Modified: Tue, 04 Nov 2025 12:28:42 GMT  
		Size: 2.7 MB (2670678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d6fd9310c7e66f30a7ba0c380f7120eebd9bddc8954c3331a6ac84e37f7b8f`  
		Last Modified: Tue, 04 Nov 2025 12:28:43 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:e4adbc03b222b4c68855d4ee1f96d0b992308786ddb56edb084b88509cc71082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81625897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c625c6a2ff15b8fa5f39304719292233d4182c4da0eaaba3db545a9411241816`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:46:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 00:49:08 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:49:08 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 00:49:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 00:49:08 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 00:49:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 00:49:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 00:49:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:49:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 00:49:08 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 01:50:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 01:50:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 01:50:37 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 01:50:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 01:50:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 01:50:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 01:50:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 01:50:37 GMT
USER fluent
# Tue, 04 Nov 2025 01:50:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3823f037b70c41ecc00a6f2d0b2fc7263b297058c445125961e26de8d7c135e`  
		Last Modified: Tue, 04 Nov 2025 00:49:26 GMT  
		Size: 3.3 MB (3340651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1dcbe472a4cca517cbccfe184a251cefd7ea2fb2da816f093f160c41459d44`  
		Last Modified: Tue, 04 Nov 2025 00:49:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6008555cb6452b9452f147f6d1ad2bf84b8c481b20faef205092ec5e24e00a25`  
		Last Modified: Tue, 04 Nov 2025 00:49:31 GMT  
		Size: 35.9 MB (35900683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b367beaf9ba47acfcfc3e846f7f9ccbd42d39e8852aa84b2af263c04d5295e1d`  
		Last Modified: Tue, 04 Nov 2025 00:49:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faa3d68d3a0b14aacf7c5570bed6dfb57ff38379784b07fd88cf8a833c9bcb2`  
		Last Modified: Tue, 04 Nov 2025 01:50:50 GMT  
		Size: 14.3 MB (14279802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e41a4701bd60b9bec299db3a3adf87d11622c82d15bca509ab94650efc0bbe3`  
		Last Modified: Tue, 04 Nov 2025 01:50:50 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97600259c6fd4b1eae341aac6d964e2eb9162e9a08f93d4751eb8a1b8f89ee38`  
		Last Modified: Tue, 04 Nov 2025 01:50:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8cf4bcb6880345f8f199a06190bc2e998b75a9dbd7370098094fc614d15358`  
		Last Modified: Tue, 04 Nov 2025 01:50:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5a10aecbde71e7cb9b49529bdc27967eb1beb10b450df81d980767e20252256b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f545406e00fdad723a3768058d6a3f51b60dc54c2fc44a95782dd618ab529d1`

```dockerfile
```

-	Layers:
	-	`sha256:b21d6a059cf580534938c8239845abe581fe6f59e1feedf02ea5228d2c28ee70`  
		Last Modified: Tue, 04 Nov 2025 12:28:47 GMT  
		Size: 2.7 MB (2668692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec52797ff3d9bf09e72847fa82e8fb6e0edbe9010a30abdeb39cb19e1abee9d`  
		Last Modified: Tue, 04 Nov 2025 12:28:47 GMT  
		Size: 21.2 KB (21156 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5df4e8b2e830a5003333e290ce271796fdfc7bf162a3fa4a7128ed51cfef0686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23bc26f4db07b606df02f14ce3b529bd3b232e9d0dc8e86d66bebd934352301`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:40:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 03:45:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:45:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:45:47 GMT
CMD ["irb"]
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:22:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 18 Nov 2025 05:22:34 GMT
ENV TINI_VERSION=0.18.0
# Tue, 18 Nov 2025 05:22:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:22:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:22:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:22:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:22:34 GMT
USER fluent
# Tue, 18 Nov 2025 05:22:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:22:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ae260a61c110779bd438deac4d1cd76065ff2394ea83afc9ff5529ea91071`  
		Last Modified: Tue, 18 Nov 2025 03:42:47 GMT  
		Size: 3.5 MB (3510984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356fe9a31a02a164458a68e3f079e86eabe6530bc2f61ae1772c93ea96dfa2a`  
		Last Modified: Tue, 18 Nov 2025 03:42:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0b280db48ee6f86ec56584743697a062ecc6953d4df02a3fe330846b9913a`  
		Last Modified: Tue, 18 Nov 2025 03:46:03 GMT  
		Size: 32.2 MB (32160063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23894894335470a52957a4ef6504faf802a94d333679fd77a4c50a500ae296d0`  
		Last Modified: Tue, 18 Nov 2025 03:46:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979287a7b7479f4b091297b8dde77dd57c16255c1122c316d64dc56986cbe84a`  
		Last Modified: Tue, 18 Nov 2025 05:22:51 GMT  
		Size: 14.1 MB (14066199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daafd6d338e29911ba2ed0bb0dc4f03149fa5d57f96910e6062ca814f1d2cb`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a19ba85eb93000ad493ae17988dc6f1cebc1b849fe17484acbca51ea4e25ea`  
		Last Modified: Tue, 18 Nov 2025 05:22:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757e96ba36c6bae804639ca2dadf2349a78d93393529d6377d411a1e46eb13e2`  
		Last Modified: Tue, 18 Nov 2025 05:22:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3e0f8b5b437688f58383aa7bbf12ccce82a250f7adc1aaea24df67d02376cd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97badbe75c72a0883ff7fa244c548058584d26342bdbe2a1a40dd9da77026744`

```dockerfile
```

-	Layers:
	-	`sha256:9c8cce8e3dfe4cce97ae219a474956647bbc2d50d4f9c0348172ec67f4c23f8b`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 2.7 MB (2665631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcee889ac2455f6b2a0a490ac2e27e5e15a2c2abafd1f3913fbfb7a83acea5f`  
		Last Modified: Tue, 18 Nov 2025 06:32:22 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:a38d80ee2741c444bb4d78eec39c472e7142555a187977719b810e56737eaa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84284683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c1025723ca160e4657f60b6f4a0af2a0e357eaf312ec7a43e3044990f804da`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 12:21:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 12:21:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:52:48 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:52:48 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 12:52:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 12:52:48 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 12:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:52:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:52:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:52:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:52:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:52:49 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:52:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:52:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 19:52:43 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 19:52:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:52:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:52:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:52:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:52:44 GMT
USER fluent
# Tue, 04 Nov 2025 19:52:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:52:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8143fbf0f893350a0d0f8d7e79c8f5671506d0e0a728c087e659b8953f7c93e4`  
		Last Modified: Tue, 04 Nov 2025 12:25:39 GMT  
		Size: 3.7 MB (3709076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b9de7bb388d880720eef9fc2101448ebf22fa5da782c4633dc51c9571b3fa`  
		Last Modified: Tue, 04 Nov 2025 12:25:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326d61f4903134b5057582473b8ba1ad2092eb821b96d773d749a73fce65bcb6`  
		Last Modified: Tue, 04 Nov 2025 12:53:30 GMT  
		Size: 33.8 MB (33832724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8de2c39c8617763720d792c9cdba652f68a35fd74e12df5f03d24fe74ce1209`  
		Last Modified: Tue, 04 Nov 2025 12:53:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a7798e76604a4dd7505fd04cbb6218980d9b6d02ad79ec9e987a8bdb973b5`  
		Last Modified: Tue, 04 Nov 2025 19:53:31 GMT  
		Size: 14.7 MB (14671591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4a87ab8faffe3819a8b2c92392409d8a8b687a425c3c81a19767f21dd680f`  
		Last Modified: Tue, 04 Nov 2025 19:53:29 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59960f93e0d6e004964b590a19fce8832fbcd20804ee0112b8631c36d41008a9`  
		Last Modified: Tue, 04 Nov 2025 19:53:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5f4b0401b5e9251cf47c9fb6e6289c3eb03a62abbf604d19527979d60e266c`  
		Last Modified: Tue, 04 Nov 2025 19:53:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3dbffe8c2c68790680a1b3fd2d1cc26b9e420ab4b14bfd93d4616aa030f808dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef226def38f94add13edbc27c0ba7b4732b1ff1269959b7539aafc20560b31ff`

```dockerfile
```

-	Layers:
	-	`sha256:28104fbc29223a553ad8b546b3f4b3743b108952f858a7412f2c2e0e2e586fb5`  
		Last Modified: Tue, 04 Nov 2025 21:28:43 GMT  
		Size: 2.7 MB (2672869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8560342a4a2268ae1a24a54c0b2046e25ff5763a87f2cb8c0b9bf892f31939ec`  
		Last Modified: Tue, 04 Nov 2025 21:28:44 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:5992a68f45d51d6f99314b75f2bb91c3ace61db1a745b1c2900cc4cf1ec9bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bfeed593c818f2c455874423d250b6b14382e85d23431a94b18fc5b1abcc93`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:02:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 06:13:39 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:13:39 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 04 Nov 2025 06:13:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 04 Nov 2025 06:13:39 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 04 Nov 2025 06:13:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 06:13:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 06:13:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 06:13:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:13:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 06:13:39 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:49:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:49:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Tue, 04 Nov 2025 16:49:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Nov 2025 16:49:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:49:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:49:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:49:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:49:36 GMT
USER fluent
# Tue, 04 Nov 2025 16:49:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:49:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2508423c296a194164ad7e8012377ae140ab815233294177a81d624e5b13a37f`  
		Last Modified: Tue, 04 Nov 2025 06:04:55 GMT  
		Size: 3.2 MB (3170294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2434e8e8caf77576c0fe5d3fae1e9e026b80c16b8591fd2d5c34c60b2f7357b`  
		Last Modified: Tue, 04 Nov 2025 06:04:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619f8637cfe20a673bd0eed22af0c0ebed0146411e746709a6dfa9286eed16b6`  
		Last Modified: Tue, 04 Nov 2025 06:14:03 GMT  
		Size: 33.1 MB (33099333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1f7b8806e6bb69ec6303f9e1cf2741a10643fab10adbfecc7911cdd8c42cff`  
		Last Modified: Tue, 04 Nov 2025 06:14:01 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37497bcdd36e54fec25e6ad5e250014e87d26ff144feba42000fd8fd47673533`  
		Last Modified: Tue, 04 Nov 2025 16:50:01 GMT  
		Size: 14.4 MB (14408192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e4ddcd3465e4c02dc022bbc8fc6138a9c64a4e186bbe8d0765dec43b1ed73f`  
		Last Modified: Tue, 04 Nov 2025 16:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace6271687afe97f2c9d39256c9973c2f6dbc78dffeab237ea67484cacf29d30`  
		Last Modified: Tue, 04 Nov 2025 16:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3fc37ab0266a9acd2af0ca50d0df899e270162904a34503a1722fc954336e8`  
		Last Modified: Tue, 04 Nov 2025 16:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b6a6af06f63b7889d10a7125c144af5109914a5d108af5c7a218a8945afc05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b99451d889163960c9765b4b1468d70ad3e9b262d1ba651a43de32e813e8095`

```dockerfile
```

-	Layers:
	-	`sha256:c262a5feb2433c116c299777c925191d9b9fcf4b364ebbc302ca58e976ce7475`  
		Last Modified: Tue, 04 Nov 2025 18:28:51 GMT  
		Size: 2.7 MB (2665277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22cd35899d433493177bf4e9297bdacb223f97baa39141c96bc04576cb64520a`  
		Last Modified: Tue, 04 Nov 2025 18:28:52 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:8cf29dd79923e5b563ae2095db9db02320afa4da54e353acc0909e48c9ad4598
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
$ docker pull fluentd@sha256:7819416a79c16651791d8bc33c3d2d2bacccae796b2d58770eef22cae6934ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79263253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c2fd4acd09b8114f6adaad9f0a061339841357d75b38302a422e22d2cf71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 07:56:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 07:56:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 07:56:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 07:56:47 GMT
USER fluent
# Tue, 04 Nov 2025 07:56:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16a280ca2b46af513537a7d977a24dd0779f3b6b7ac2a379e32564f36bb62f`  
		Last Modified: Tue, 04 Nov 2025 04:29:35 GMT  
		Size: 1.3 MB (1279642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12677bb7810189f862e4324fd378db9bc131cf8446805bdcf9923ad09d03c85`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e12593a63e3781635232c1a24a87ca6d97150b8e568eaf8b52786ec55eeb71`  
		Last Modified: Tue, 04 Nov 2025 04:29:38 GMT  
		Size: 42.2 MB (42158201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06499c8b4d3f65803507338e343bb0c0eb7ef53c593e6346ab9acb506fd6234`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27dc8130de8c329d0a0c9f1c320445f464a342eeb7f063813ab0795d768eab1`  
		Last Modified: Tue, 04 Nov 2025 07:57:02 GMT  
		Size: 6.0 MB (6044919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84612fac3accfb10321a8fe2ca5683b31586a4b08497cd6e4d5fc2af03946b74`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95792bf9a95a58f0406cece5a0f922c7a14b54d4f7b0df84dec66681318c7f`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a524cc95e962099ab0a7ea84fc877a450f98399087903f4f5952648f8103d1`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a15d99c368e421dc0bec89ac4bea53a7b5e3fb28994944ce9205dca48d2661b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964096aad19d9289aacb375444671cad9a090d9c902fe5aad199190dcc630703`

```dockerfile
```

-	Layers:
	-	`sha256:6918ed07569ebd6b8095f181ae6eb385f22aa81af468c74a7e0b6e6e30d1e9ce`  
		Last Modified: Tue, 04 Nov 2025 09:28:27 GMT  
		Size: 2.3 MB (2283564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed68f47f9b6c0beb0b780aac2d7d516a0badcbf467db435bde84defa983cdd8`  
		Last Modified: Tue, 04 Nov 2025 09:28:28 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
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
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
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
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:544e4c0d4869ab3260580ecc06084b2ced7e4a6f01a2241d3dcc84aff57415a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce55aad25aee0631fc7e542c25999e2a3222438f483fe8a8070a7dcb9c49f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 03:44:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:44:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:44:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:44:57 GMT
USER fluent
# Tue, 04 Nov 2025 03:44:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff1cf61353f8dff587184978fed1cbb398dca8e140da33c564fefaec487d2e`  
		Last Modified: Tue, 04 Nov 2025 02:36:44 GMT  
		Size: 1.2 MB (1236604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff3a12ca516b6f79cbac115ae27bcbb967dd1009cccff770d79a7cae383a3f`  
		Last Modified: Tue, 04 Nov 2025 02:36:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6468f7034188523d195654f6c0fb84c8d7d944289ae9e8f031cb5f78c7a580`  
		Last Modified: Tue, 04 Nov 2025 02:39:45 GMT  
		Size: 37.9 MB (37865491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950069925d30b01ded0a2ed186d917f1eff55fd5881f4be0b9d79cf4398aee27`  
		Last Modified: Tue, 04 Nov 2025 02:39:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861110680e1af462aee0aeffd9bb605f97301dfbacee73847bdbbfc8d45eff00`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 5.7 MB (5706065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9eeb05f20b9801ce1491ceac4a4721fad3184d46b7e5829d4ea70dec205204`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cf759dc69023991dabc97ed97c90d836d0080e04dc6e31eee3154c3e63bc`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaee8cdfbeb1c9562699525af9ea90ae4fb972270008cf3c8d09afce225ff4d`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:81151156ca085b78155762060cf4e8475f93f3c8a634c3fc05b75eaf2f1cbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42bb9185d066277fd1c662f181dd3d98d74f982179b66658d8044bd8483a68a`

```dockerfile
```

-	Layers:
	-	`sha256:b1d298e7774fea3ebb0f378680fd9fe5a7227345f1e92d8a8f5bb7561b0230f9`  
		Last Modified: Tue, 04 Nov 2025 12:28:29 GMT  
		Size: 2.3 MB (2284976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f942b31474bfce92005254c89e81053a0b334f42328c9c7b3ebd0d56bd8c2606`  
		Last Modified: Tue, 04 Nov 2025 12:28:30 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:91b6b4da2fc6090374e0fda11e524d15864879c72ab8ea891305c6a5dcc6f8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79582515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7ede2b923eb0046c874d79a45ff044f0476e7c68dc32b7025c20e8b4e2e79e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 02:37:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 02:37:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 02:37:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 02:37:13 GMT
USER fluent
# Tue, 04 Nov 2025 02:37:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 02:37:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c83755afbe771e645a69fd11df0a60d6e7dd541fc57e5b0f1b0be4b2a0883`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 1.3 MB (1261429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c48599929aa6c7fb7bed5f82a13c0154ffb885b6f1e85e9f644b0767b1f70`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e552b7b884adedf291e273039ac04ca2d02aac2bf91d0790d8ed1417002926`  
		Last Modified: Tue, 04 Nov 2025 01:42:15 GMT  
		Size: 42.1 MB (42145432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35feb980ed30f707dcd311800ab0801ef0c69e411a8513d2d57f4e74def26a3`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3b50e47c048e589ed069424290b2dadff117a2cfb2306543d6ea53432fdb`  
		Last Modified: Tue, 04 Nov 2025 02:37:29 GMT  
		Size: 6.0 MB (6030973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb7f246be820a9a7035411437ec82adb7b7e57751074a838dcb8b57853e218`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fee3af5dc401f90c63aff5571b43de11c5e287af015286ceac268d59823fb`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b82136c4c34e431e87e862f28be1d30faf08715c8265f07c8c6c3f747472b0`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:12d71120b81b51551d597b9ce196c3ad25405bb7534bb306d9695e728dbe357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184e9b9694fc38927b46e669811d5a4188b127fdbfb32a2c12b823816eb472b3`

```dockerfile
```

-	Layers:
	-	`sha256:9af4c91c515dc26f2329814b50546b04473222e4ebe2c4a0c84c607529966896`  
		Last Modified: Tue, 04 Nov 2025 12:28:33 GMT  
		Size: 2.3 MB (2283836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff4bfd853e2bbafcd8a04cb7af0cf640464cbeddc807c9e1758691418aa7f0d`  
		Last Modified: Tue, 04 Nov 2025 12:28:34 GMT  
		Size: 21.2 KB (21231 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
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
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
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
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0394134b4106e1a322bc5bea388bc8ea50ff54a9ec059144495d0a36ce1895e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81071254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4416a657be5c504ac27d0c7cfc006b240f8440de7467c80ea69c3bc92deb14`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:16:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:30:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:30:05 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 19:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:58:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:58:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:58:41 GMT
USER fluent
# Tue, 04 Nov 2025 19:58:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:58:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7cafc9e521290ae17ae96071a62fa0ce9cc48a489bf957fdf15c09abb8a804`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 1.3 MB (1310384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74df3c614cf044979896d45fdbb3780600a0f2a6f1a699a70de10d0153e6928`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312abe5d4cfc4eeefc5f2b09f01e9ba77dc6e592a8edc74346d8a87f2e45f28`  
		Last Modified: Tue, 04 Nov 2025 12:31:03 GMT  
		Size: 39.6 MB (39601068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf418f7fe1d0352a8b07d3730b4a8393da06df977da19a9696aee08825025762`  
		Last Modified: Tue, 04 Nov 2025 12:31:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091f8580ca0d0137a62e83860303b48b10b634f2bf8c18920dc53938f130c40`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 6.6 MB (6558759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718bc6b50d295b1fd485e209c3ff74421802ebc3cf2cef01b33cb7da8e34b56d`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd40aa235056c26c6f0ae37c8933e1bb288034d9df402cc18252f6469055634`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7206d908d6189a487af234889268cf4d47da74c4477a00e4cfd36716b4da41`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fae67ad3e796f6f0ecc8f62eb44739b84e730d986fd6ad5f24529f7d2d9f5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb05857bad1224261621c7abf7b6d6c484c2426724863ca259d07ec32a30073`

```dockerfile
```

-	Layers:
	-	`sha256:c37622be462407f9cc248533cbe5481f7f58bdfa498235b22b4fa1c6d44c5e02`  
		Last Modified: Tue, 04 Nov 2025 21:28:33 GMT  
		Size: 2.3 MB (2287099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb120fc15050a9d25f652c7c39a98e10d98d3dcaff6ec871e1c195547104024d`  
		Last Modified: Tue, 04 Nov 2025 21:28:34 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:1ba5ab678ead4498d917c4a7acd915ded9543f724cca2e527022ac6d159ca302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76838773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b70ec958c85adaa042b79d68f9db29879abdda7e2a6d46e6a9abd70dcff705`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:39:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:46:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:46:17 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 16:53:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:53:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:53:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:53:20 GMT
USER fluent
# Tue, 04 Nov 2025 16:53:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:53:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc87d0d125756f6f7207ff00dd475820f1f662c1490e4f973570b5313e17fb6`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 1.3 MB (1294636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7ffedbe0c72a7402c4c7ffa7ad05e05878b479406400dca12509798aee65e`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f9a0ba0eb1a5da7986fb92d450451bc333572015535b1b763a366214e8b6b`  
		Last Modified: Tue, 04 Nov 2025 12:47:04 GMT  
		Size: 39.3 MB (39287395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46ca528085c3652d506f94d3950096f37aeec2bac6827ae4ff7383b0116b3a`  
		Last Modified: Tue, 04 Nov 2025 12:47:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa746dbbf4325707691bffabcca7d685a3cc3583cfe8ab8fbf04e6277f7aa0`  
		Last Modified: Tue, 04 Nov 2025 16:53:53 GMT  
		Size: 6.4 MB (6416957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8612a12f56f9dd86f9543a9f598cbf2d6a78e2b2142aa806819ba55ce2e4c`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9830c4ec73592c4e33e871e27ce42c0d59915736cb3509bce80fa989224d30d4`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5636653a1ba6f2e97b635e9f1431d02cdd51383519faadd8db32a4d63b5c29`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc22a7b6537fcb04e3c6a4e56db9d883c06682e2e189a1b2234c412a224936fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee2879aa877fd3fc5831fc029db676d66d3e506782f7f836964f6b7b70dbbe2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d17eac27b3fcd0ccc656c80d3b5611487691fa4010b7bd570558181bcc774`  
		Last Modified: Tue, 04 Nov 2025 18:28:41 GMT  
		Size: 2.3 MB (2285009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327e0a83092a2b5e6b90c9f10c9f4cfd2fa1541fbcd2bbaa1a46c3b6057c9f1d`  
		Last Modified: Tue, 04 Nov 2025 18:28:42 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:8cf29dd79923e5b563ae2095db9db02320afa4da54e353acc0909e48c9ad4598
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
$ docker pull fluentd@sha256:7819416a79c16651791d8bc33c3d2d2bacccae796b2d58770eef22cae6934ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79263253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c2fd4acd09b8114f6adaad9f0a061339841357d75b38302a422e22d2cf71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 07:56:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 07:56:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 07:56:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 07:56:47 GMT
USER fluent
# Tue, 04 Nov 2025 07:56:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16a280ca2b46af513537a7d977a24dd0779f3b6b7ac2a379e32564f36bb62f`  
		Last Modified: Tue, 04 Nov 2025 04:29:35 GMT  
		Size: 1.3 MB (1279642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12677bb7810189f862e4324fd378db9bc131cf8446805bdcf9923ad09d03c85`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e12593a63e3781635232c1a24a87ca6d97150b8e568eaf8b52786ec55eeb71`  
		Last Modified: Tue, 04 Nov 2025 04:29:38 GMT  
		Size: 42.2 MB (42158201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06499c8b4d3f65803507338e343bb0c0eb7ef53c593e6346ab9acb506fd6234`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27dc8130de8c329d0a0c9f1c320445f464a342eeb7f063813ab0795d768eab1`  
		Last Modified: Tue, 04 Nov 2025 07:57:02 GMT  
		Size: 6.0 MB (6044919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84612fac3accfb10321a8fe2ca5683b31586a4b08497cd6e4d5fc2af03946b74`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95792bf9a95a58f0406cece5a0f922c7a14b54d4f7b0df84dec66681318c7f`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a524cc95e962099ab0a7ea84fc877a450f98399087903f4f5952648f8103d1`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a15d99c368e421dc0bec89ac4bea53a7b5e3fb28994944ce9205dca48d2661b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964096aad19d9289aacb375444671cad9a090d9c902fe5aad199190dcc630703`

```dockerfile
```

-	Layers:
	-	`sha256:6918ed07569ebd6b8095f181ae6eb385f22aa81af468c74a7e0b6e6e30d1e9ce`  
		Last Modified: Tue, 04 Nov 2025 09:28:27 GMT  
		Size: 2.3 MB (2283564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed68f47f9b6c0beb0b780aac2d7d516a0badcbf467db435bde84defa983cdd8`  
		Last Modified: Tue, 04 Nov 2025 09:28:28 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
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
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
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
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:544e4c0d4869ab3260580ecc06084b2ced7e4a6f01a2241d3dcc84aff57415a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce55aad25aee0631fc7e542c25999e2a3222438f483fe8a8070a7dcb9c49f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 03:44:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:44:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:44:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:44:57 GMT
USER fluent
# Tue, 04 Nov 2025 03:44:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff1cf61353f8dff587184978fed1cbb398dca8e140da33c564fefaec487d2e`  
		Last Modified: Tue, 04 Nov 2025 02:36:44 GMT  
		Size: 1.2 MB (1236604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff3a12ca516b6f79cbac115ae27bcbb967dd1009cccff770d79a7cae383a3f`  
		Last Modified: Tue, 04 Nov 2025 02:36:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6468f7034188523d195654f6c0fb84c8d7d944289ae9e8f031cb5f78c7a580`  
		Last Modified: Tue, 04 Nov 2025 02:39:45 GMT  
		Size: 37.9 MB (37865491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950069925d30b01ded0a2ed186d917f1eff55fd5881f4be0b9d79cf4398aee27`  
		Last Modified: Tue, 04 Nov 2025 02:39:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861110680e1af462aee0aeffd9bb605f97301dfbacee73847bdbbfc8d45eff00`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 5.7 MB (5706065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9eeb05f20b9801ce1491ceac4a4721fad3184d46b7e5829d4ea70dec205204`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cf759dc69023991dabc97ed97c90d836d0080e04dc6e31eee3154c3e63bc`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaee8cdfbeb1c9562699525af9ea90ae4fb972270008cf3c8d09afce225ff4d`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:81151156ca085b78155762060cf4e8475f93f3c8a634c3fc05b75eaf2f1cbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42bb9185d066277fd1c662f181dd3d98d74f982179b66658d8044bd8483a68a`

```dockerfile
```

-	Layers:
	-	`sha256:b1d298e7774fea3ebb0f378680fd9fe5a7227345f1e92d8a8f5bb7561b0230f9`  
		Last Modified: Tue, 04 Nov 2025 12:28:29 GMT  
		Size: 2.3 MB (2284976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f942b31474bfce92005254c89e81053a0b334f42328c9c7b3ebd0d56bd8c2606`  
		Last Modified: Tue, 04 Nov 2025 12:28:30 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:91b6b4da2fc6090374e0fda11e524d15864879c72ab8ea891305c6a5dcc6f8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79582515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7ede2b923eb0046c874d79a45ff044f0476e7c68dc32b7025c20e8b4e2e79e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 02:37:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 02:37:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 02:37:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 02:37:13 GMT
USER fluent
# Tue, 04 Nov 2025 02:37:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 02:37:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c83755afbe771e645a69fd11df0a60d6e7dd541fc57e5b0f1b0be4b2a0883`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 1.3 MB (1261429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c48599929aa6c7fb7bed5f82a13c0154ffb885b6f1e85e9f644b0767b1f70`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e552b7b884adedf291e273039ac04ca2d02aac2bf91d0790d8ed1417002926`  
		Last Modified: Tue, 04 Nov 2025 01:42:15 GMT  
		Size: 42.1 MB (42145432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35feb980ed30f707dcd311800ab0801ef0c69e411a8513d2d57f4e74def26a3`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3b50e47c048e589ed069424290b2dadff117a2cfb2306543d6ea53432fdb`  
		Last Modified: Tue, 04 Nov 2025 02:37:29 GMT  
		Size: 6.0 MB (6030973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb7f246be820a9a7035411437ec82adb7b7e57751074a838dcb8b57853e218`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fee3af5dc401f90c63aff5571b43de11c5e287af015286ceac268d59823fb`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b82136c4c34e431e87e862f28be1d30faf08715c8265f07c8c6c3f747472b0`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:12d71120b81b51551d597b9ce196c3ad25405bb7534bb306d9695e728dbe357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184e9b9694fc38927b46e669811d5a4188b127fdbfb32a2c12b823816eb472b3`

```dockerfile
```

-	Layers:
	-	`sha256:9af4c91c515dc26f2329814b50546b04473222e4ebe2c4a0c84c607529966896`  
		Last Modified: Tue, 04 Nov 2025 12:28:33 GMT  
		Size: 2.3 MB (2283836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff4bfd853e2bbafcd8a04cb7af0cf640464cbeddc807c9e1758691418aa7f0d`  
		Last Modified: Tue, 04 Nov 2025 12:28:34 GMT  
		Size: 21.2 KB (21231 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
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
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
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
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0394134b4106e1a322bc5bea388bc8ea50ff54a9ec059144495d0a36ce1895e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81071254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4416a657be5c504ac27d0c7cfc006b240f8440de7467c80ea69c3bc92deb14`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:16:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:30:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:30:05 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 19:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:58:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:58:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:58:41 GMT
USER fluent
# Tue, 04 Nov 2025 19:58:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:58:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7cafc9e521290ae17ae96071a62fa0ce9cc48a489bf957fdf15c09abb8a804`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 1.3 MB (1310384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74df3c614cf044979896d45fdbb3780600a0f2a6f1a699a70de10d0153e6928`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312abe5d4cfc4eeefc5f2b09f01e9ba77dc6e592a8edc74346d8a87f2e45f28`  
		Last Modified: Tue, 04 Nov 2025 12:31:03 GMT  
		Size: 39.6 MB (39601068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf418f7fe1d0352a8b07d3730b4a8393da06df977da19a9696aee08825025762`  
		Last Modified: Tue, 04 Nov 2025 12:31:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091f8580ca0d0137a62e83860303b48b10b634f2bf8c18920dc53938f130c40`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 6.6 MB (6558759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718bc6b50d295b1fd485e209c3ff74421802ebc3cf2cef01b33cb7da8e34b56d`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd40aa235056c26c6f0ae37c8933e1bb288034d9df402cc18252f6469055634`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7206d908d6189a487af234889268cf4d47da74c4477a00e4cfd36716b4da41`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fae67ad3e796f6f0ecc8f62eb44739b84e730d986fd6ad5f24529f7d2d9f5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb05857bad1224261621c7abf7b6d6c484c2426724863ca259d07ec32a30073`

```dockerfile
```

-	Layers:
	-	`sha256:c37622be462407f9cc248533cbe5481f7f58bdfa498235b22b4fa1c6d44c5e02`  
		Last Modified: Tue, 04 Nov 2025 21:28:33 GMT  
		Size: 2.3 MB (2287099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb120fc15050a9d25f652c7c39a98e10d98d3dcaff6ec871e1c195547104024d`  
		Last Modified: Tue, 04 Nov 2025 21:28:34 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:1ba5ab678ead4498d917c4a7acd915ded9543f724cca2e527022ac6d159ca302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76838773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b70ec958c85adaa042b79d68f9db29879abdda7e2a6d46e6a9abd70dcff705`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:39:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:46:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:46:17 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 16:53:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:53:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:53:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:53:20 GMT
USER fluent
# Tue, 04 Nov 2025 16:53:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:53:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc87d0d125756f6f7207ff00dd475820f1f662c1490e4f973570b5313e17fb6`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 1.3 MB (1294636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7ffedbe0c72a7402c4c7ffa7ad05e05878b479406400dca12509798aee65e`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f9a0ba0eb1a5da7986fb92d450451bc333572015535b1b763a366214e8b6b`  
		Last Modified: Tue, 04 Nov 2025 12:47:04 GMT  
		Size: 39.3 MB (39287395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46ca528085c3652d506f94d3950096f37aeec2bac6827ae4ff7383b0116b3a`  
		Last Modified: Tue, 04 Nov 2025 12:47:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa746dbbf4325707691bffabcca7d685a3cc3583cfe8ab8fbf04e6277f7aa0`  
		Last Modified: Tue, 04 Nov 2025 16:53:53 GMT  
		Size: 6.4 MB (6416957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8612a12f56f9dd86f9543a9f598cbf2d6a78e2b2142aa806819ba55ce2e4c`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9830c4ec73592c4e33e871e27ce42c0d59915736cb3509bce80fa989224d30d4`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5636653a1ba6f2e97b635e9f1431d02cdd51383519faadd8db32a4d63b5c29`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc22a7b6537fcb04e3c6a4e56db9d883c06682e2e189a1b2234c412a224936fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee2879aa877fd3fc5831fc029db676d66d3e506782f7f836964f6b7b70dbbe2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d17eac27b3fcd0ccc656c80d3b5611487691fa4010b7bd570558181bcc774`  
		Last Modified: Tue, 04 Nov 2025 18:28:41 GMT  
		Size: 2.3 MB (2285009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327e0a83092a2b5e6b90c9f10c9f4cfd2fa1541fbcd2bbaa1a46c3b6057c9f1d`  
		Last Modified: Tue, 04 Nov 2025 18:28:42 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:8cf29dd79923e5b563ae2095db9db02320afa4da54e353acc0909e48c9ad4598
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
$ docker pull fluentd@sha256:7819416a79c16651791d8bc33c3d2d2bacccae796b2d58770eef22cae6934ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79263253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c2fd4acd09b8114f6adaad9f0a061339841357d75b38302a422e22d2cf71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 07:56:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 07:56:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 07:56:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 07:56:47 GMT
USER fluent
# Tue, 04 Nov 2025 07:56:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16a280ca2b46af513537a7d977a24dd0779f3b6b7ac2a379e32564f36bb62f`  
		Last Modified: Tue, 04 Nov 2025 04:29:35 GMT  
		Size: 1.3 MB (1279642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12677bb7810189f862e4324fd378db9bc131cf8446805bdcf9923ad09d03c85`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e12593a63e3781635232c1a24a87ca6d97150b8e568eaf8b52786ec55eeb71`  
		Last Modified: Tue, 04 Nov 2025 04:29:38 GMT  
		Size: 42.2 MB (42158201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06499c8b4d3f65803507338e343bb0c0eb7ef53c593e6346ab9acb506fd6234`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27dc8130de8c329d0a0c9f1c320445f464a342eeb7f063813ab0795d768eab1`  
		Last Modified: Tue, 04 Nov 2025 07:57:02 GMT  
		Size: 6.0 MB (6044919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84612fac3accfb10321a8fe2ca5683b31586a4b08497cd6e4d5fc2af03946b74`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95792bf9a95a58f0406cece5a0f922c7a14b54d4f7b0df84dec66681318c7f`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a524cc95e962099ab0a7ea84fc877a450f98399087903f4f5952648f8103d1`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a15d99c368e421dc0bec89ac4bea53a7b5e3fb28994944ce9205dca48d2661b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964096aad19d9289aacb375444671cad9a090d9c902fe5aad199190dcc630703`

```dockerfile
```

-	Layers:
	-	`sha256:6918ed07569ebd6b8095f181ae6eb385f22aa81af468c74a7e0b6e6e30d1e9ce`  
		Last Modified: Tue, 04 Nov 2025 09:28:27 GMT  
		Size: 2.3 MB (2283564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed68f47f9b6c0beb0b780aac2d7d516a0badcbf467db435bde84defa983cdd8`  
		Last Modified: Tue, 04 Nov 2025 09:28:28 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
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
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
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
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:544e4c0d4869ab3260580ecc06084b2ced7e4a6f01a2241d3dcc84aff57415a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce55aad25aee0631fc7e542c25999e2a3222438f483fe8a8070a7dcb9c49f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 03:44:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:44:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:44:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:44:57 GMT
USER fluent
# Tue, 04 Nov 2025 03:44:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff1cf61353f8dff587184978fed1cbb398dca8e140da33c564fefaec487d2e`  
		Last Modified: Tue, 04 Nov 2025 02:36:44 GMT  
		Size: 1.2 MB (1236604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff3a12ca516b6f79cbac115ae27bcbb967dd1009cccff770d79a7cae383a3f`  
		Last Modified: Tue, 04 Nov 2025 02:36:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6468f7034188523d195654f6c0fb84c8d7d944289ae9e8f031cb5f78c7a580`  
		Last Modified: Tue, 04 Nov 2025 02:39:45 GMT  
		Size: 37.9 MB (37865491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950069925d30b01ded0a2ed186d917f1eff55fd5881f4be0b9d79cf4398aee27`  
		Last Modified: Tue, 04 Nov 2025 02:39:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861110680e1af462aee0aeffd9bb605f97301dfbacee73847bdbbfc8d45eff00`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 5.7 MB (5706065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9eeb05f20b9801ce1491ceac4a4721fad3184d46b7e5829d4ea70dec205204`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cf759dc69023991dabc97ed97c90d836d0080e04dc6e31eee3154c3e63bc`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaee8cdfbeb1c9562699525af9ea90ae4fb972270008cf3c8d09afce225ff4d`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:81151156ca085b78155762060cf4e8475f93f3c8a634c3fc05b75eaf2f1cbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42bb9185d066277fd1c662f181dd3d98d74f982179b66658d8044bd8483a68a`

```dockerfile
```

-	Layers:
	-	`sha256:b1d298e7774fea3ebb0f378680fd9fe5a7227345f1e92d8a8f5bb7561b0230f9`  
		Last Modified: Tue, 04 Nov 2025 12:28:29 GMT  
		Size: 2.3 MB (2284976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f942b31474bfce92005254c89e81053a0b334f42328c9c7b3ebd0d56bd8c2606`  
		Last Modified: Tue, 04 Nov 2025 12:28:30 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:91b6b4da2fc6090374e0fda11e524d15864879c72ab8ea891305c6a5dcc6f8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79582515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7ede2b923eb0046c874d79a45ff044f0476e7c68dc32b7025c20e8b4e2e79e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 02:37:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 02:37:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 02:37:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 02:37:13 GMT
USER fluent
# Tue, 04 Nov 2025 02:37:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 02:37:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c83755afbe771e645a69fd11df0a60d6e7dd541fc57e5b0f1b0be4b2a0883`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 1.3 MB (1261429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c48599929aa6c7fb7bed5f82a13c0154ffb885b6f1e85e9f644b0767b1f70`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e552b7b884adedf291e273039ac04ca2d02aac2bf91d0790d8ed1417002926`  
		Last Modified: Tue, 04 Nov 2025 01:42:15 GMT  
		Size: 42.1 MB (42145432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35feb980ed30f707dcd311800ab0801ef0c69e411a8513d2d57f4e74def26a3`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3b50e47c048e589ed069424290b2dadff117a2cfb2306543d6ea53432fdb`  
		Last Modified: Tue, 04 Nov 2025 02:37:29 GMT  
		Size: 6.0 MB (6030973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb7f246be820a9a7035411437ec82adb7b7e57751074a838dcb8b57853e218`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fee3af5dc401f90c63aff5571b43de11c5e287af015286ceac268d59823fb`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b82136c4c34e431e87e862f28be1d30faf08715c8265f07c8c6c3f747472b0`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:12d71120b81b51551d597b9ce196c3ad25405bb7534bb306d9695e728dbe357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184e9b9694fc38927b46e669811d5a4188b127fdbfb32a2c12b823816eb472b3`

```dockerfile
```

-	Layers:
	-	`sha256:9af4c91c515dc26f2329814b50546b04473222e4ebe2c4a0c84c607529966896`  
		Last Modified: Tue, 04 Nov 2025 12:28:33 GMT  
		Size: 2.3 MB (2283836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff4bfd853e2bbafcd8a04cb7af0cf640464cbeddc807c9e1758691418aa7f0d`  
		Last Modified: Tue, 04 Nov 2025 12:28:34 GMT  
		Size: 21.2 KB (21231 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
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
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
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
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0394134b4106e1a322bc5bea388bc8ea50ff54a9ec059144495d0a36ce1895e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81071254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4416a657be5c504ac27d0c7cfc006b240f8440de7467c80ea69c3bc92deb14`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:16:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:30:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:30:05 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 19:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:58:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:58:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:58:41 GMT
USER fluent
# Tue, 04 Nov 2025 19:58:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:58:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7cafc9e521290ae17ae96071a62fa0ce9cc48a489bf957fdf15c09abb8a804`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 1.3 MB (1310384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74df3c614cf044979896d45fdbb3780600a0f2a6f1a699a70de10d0153e6928`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312abe5d4cfc4eeefc5f2b09f01e9ba77dc6e592a8edc74346d8a87f2e45f28`  
		Last Modified: Tue, 04 Nov 2025 12:31:03 GMT  
		Size: 39.6 MB (39601068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf418f7fe1d0352a8b07d3730b4a8393da06df977da19a9696aee08825025762`  
		Last Modified: Tue, 04 Nov 2025 12:31:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091f8580ca0d0137a62e83860303b48b10b634f2bf8c18920dc53938f130c40`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 6.6 MB (6558759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718bc6b50d295b1fd485e209c3ff74421802ebc3cf2cef01b33cb7da8e34b56d`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd40aa235056c26c6f0ae37c8933e1bb288034d9df402cc18252f6469055634`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7206d908d6189a487af234889268cf4d47da74c4477a00e4cfd36716b4da41`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fae67ad3e796f6f0ecc8f62eb44739b84e730d986fd6ad5f24529f7d2d9f5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb05857bad1224261621c7abf7b6d6c484c2426724863ca259d07ec32a30073`

```dockerfile
```

-	Layers:
	-	`sha256:c37622be462407f9cc248533cbe5481f7f58bdfa498235b22b4fa1c6d44c5e02`  
		Last Modified: Tue, 04 Nov 2025 21:28:33 GMT  
		Size: 2.3 MB (2287099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb120fc15050a9d25f652c7c39a98e10d98d3dcaff6ec871e1c195547104024d`  
		Last Modified: Tue, 04 Nov 2025 21:28:34 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:1ba5ab678ead4498d917c4a7acd915ded9543f724cca2e527022ac6d159ca302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76838773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b70ec958c85adaa042b79d68f9db29879abdda7e2a6d46e6a9abd70dcff705`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:39:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:46:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:46:17 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 16:53:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:53:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:53:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:53:20 GMT
USER fluent
# Tue, 04 Nov 2025 16:53:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:53:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc87d0d125756f6f7207ff00dd475820f1f662c1490e4f973570b5313e17fb6`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 1.3 MB (1294636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7ffedbe0c72a7402c4c7ffa7ad05e05878b479406400dca12509798aee65e`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f9a0ba0eb1a5da7986fb92d450451bc333572015535b1b763a366214e8b6b`  
		Last Modified: Tue, 04 Nov 2025 12:47:04 GMT  
		Size: 39.3 MB (39287395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46ca528085c3652d506f94d3950096f37aeec2bac6827ae4ff7383b0116b3a`  
		Last Modified: Tue, 04 Nov 2025 12:47:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa746dbbf4325707691bffabcca7d685a3cc3583cfe8ab8fbf04e6277f7aa0`  
		Last Modified: Tue, 04 Nov 2025 16:53:53 GMT  
		Size: 6.4 MB (6416957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8612a12f56f9dd86f9543a9f598cbf2d6a78e2b2142aa806819ba55ce2e4c`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9830c4ec73592c4e33e871e27ce42c0d59915736cb3509bce80fa989224d30d4`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5636653a1ba6f2e97b635e9f1431d02cdd51383519faadd8db32a4d63b5c29`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc22a7b6537fcb04e3c6a4e56db9d883c06682e2e189a1b2234c412a224936fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee2879aa877fd3fc5831fc029db676d66d3e506782f7f836964f6b7b70dbbe2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d17eac27b3fcd0ccc656c80d3b5611487691fa4010b7bd570558181bcc774`  
		Last Modified: Tue, 04 Nov 2025 18:28:41 GMT  
		Size: 2.3 MB (2285009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327e0a83092a2b5e6b90c9f10c9f4cfd2fa1541fbcd2bbaa1a46c3b6057c9f1d`  
		Last Modified: Tue, 04 Nov 2025 18:28:42 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-debian-1.0`

```console
$ docker pull fluentd@sha256:8cf29dd79923e5b563ae2095db9db02320afa4da54e353acc0909e48c9ad4598
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
$ docker pull fluentd@sha256:7819416a79c16651791d8bc33c3d2d2bacccae796b2d58770eef22cae6934ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79263253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d49c2fd4acd09b8114f6adaad9f0a061339841357d75b38302a422e22d2cf71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:26:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 04:29:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 04:29:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 04:29:19 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 07:56:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 07:56:47 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 07:56:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 07:56:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 07:56:47 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 07:56:47 GMT
USER fluent
# Tue, 04 Nov 2025 07:56:47 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16a280ca2b46af513537a7d977a24dd0779f3b6b7ac2a379e32564f36bb62f`  
		Last Modified: Tue, 04 Nov 2025 04:29:35 GMT  
		Size: 1.3 MB (1279642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12677bb7810189f862e4324fd378db9bc131cf8446805bdcf9923ad09d03c85`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e12593a63e3781635232c1a24a87ca6d97150b8e568eaf8b52786ec55eeb71`  
		Last Modified: Tue, 04 Nov 2025 04:29:38 GMT  
		Size: 42.2 MB (42158201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06499c8b4d3f65803507338e343bb0c0eb7ef53c593e6346ab9acb506fd6234`  
		Last Modified: Tue, 04 Nov 2025 04:29:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27dc8130de8c329d0a0c9f1c320445f464a342eeb7f063813ab0795d768eab1`  
		Last Modified: Tue, 04 Nov 2025 07:57:02 GMT  
		Size: 6.0 MB (6044919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84612fac3accfb10321a8fe2ca5683b31586a4b08497cd6e4d5fc2af03946b74`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95792bf9a95a58f0406cece5a0f922c7a14b54d4f7b0df84dec66681318c7f`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a524cc95e962099ab0a7ea84fc877a450f98399087903f4f5952648f8103d1`  
		Last Modified: Tue, 04 Nov 2025 07:57:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a15d99c368e421dc0bec89ac4bea53a7b5e3fb28994944ce9205dca48d2661b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964096aad19d9289aacb375444671cad9a090d9c902fe5aad199190dcc630703`

```dockerfile
```

-	Layers:
	-	`sha256:6918ed07569ebd6b8095f181ae6eb385f22aa81af468c74a7e0b6e6e30d1e9ce`  
		Last Modified: Tue, 04 Nov 2025 09:28:27 GMT  
		Size: 2.3 MB (2283564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed68f47f9b6c0beb0b780aac2d7d516a0badcbf467db435bde84defa983cdd8`  
		Last Modified: Tue, 04 Nov 2025 09:28:28 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e8c4584c108d55ece3a65f42c824024dbf328a99081e899ff80b245b0a570eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73146995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaf0475501a66581de9ad0a42acb43b738634ecf0382206f040a53968daa0c`
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
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:35:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:35:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:35:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:35:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:35:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:35:22 GMT
USER fluent
# Tue, 18 Nov 2025 05:35:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:35:22 GMT
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
	-	`sha256:cbeefbbe12fb9ebcda2ce8336a8dd1c66bb46e2ad6411b19b7bffc9b0036457c`  
		Last Modified: Tue, 18 Nov 2025 05:35:38 GMT  
		Size: 5.9 MB (5943247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b7c342630fa0641dc5a599ec42701184fce6af1f033ca955af0e315d6f5a9`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde8aa131c4cc1ae41382dca7e8065fc0522eab2b321d2653c2be3188f7a19`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa761b7294529389f149a0dad3c5c1e134eba574c265687b6304f151605f71c`  
		Last Modified: Tue, 18 Nov 2025 05:35:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c1137d5e8fd8323f920e0b5c8c7959e672f27fd52cfbc41dbf8e03d2004af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a008dd8357b5271817dd0334598325f669c019ed411726d5c6339b6827e28f5`

```dockerfile
```

-	Layers:
	-	`sha256:08aba52ec52bd77f4a7fe5c24a8bac6440045aaf9802b32e03d3284eafb52467`  
		Last Modified: Tue, 18 Nov 2025 06:31:58 GMT  
		Size: 2.3 MB (2286529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4bbd9c3f36293e384beed646f2692b0d4805c05965214b78a20df4d56b327b`  
		Last Modified: Tue, 18 Nov 2025 06:31:59 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:544e4c0d4869ab3260580ecc06084b2ced7e4a6f01a2241d3dcc84aff57415a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce55aad25aee0631fc7e542c25999e2a3222438f483fe8a8070a7dcb9c49f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 02:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 02:39:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 02:39:26 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 03:44:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 03:44:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 03:44:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 03:44:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 03:44:57 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 03:44:57 GMT
USER fluent
# Tue, 04 Nov 2025 03:44:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff1cf61353f8dff587184978fed1cbb398dca8e140da33c564fefaec487d2e`  
		Last Modified: Tue, 04 Nov 2025 02:36:44 GMT  
		Size: 1.2 MB (1236604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff3a12ca516b6f79cbac115ae27bcbb967dd1009cccff770d79a7cae383a3f`  
		Last Modified: Tue, 04 Nov 2025 02:36:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6468f7034188523d195654f6c0fb84c8d7d944289ae9e8f031cb5f78c7a580`  
		Last Modified: Tue, 04 Nov 2025 02:39:45 GMT  
		Size: 37.9 MB (37865491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950069925d30b01ded0a2ed186d917f1eff55fd5881f4be0b9d79cf4398aee27`  
		Last Modified: Tue, 04 Nov 2025 02:39:41 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861110680e1af462aee0aeffd9bb605f97301dfbacee73847bdbbfc8d45eff00`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 5.7 MB (5706065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9eeb05f20b9801ce1491ceac4a4721fad3184d46b7e5829d4ea70dec205204`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cf759dc69023991dabc97ed97c90d836d0080e04dc6e31eee3154c3e63bc`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaee8cdfbeb1c9562699525af9ea90ae4fb972270008cf3c8d09afce225ff4d`  
		Last Modified: Tue, 04 Nov 2025 03:45:09 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:81151156ca085b78155762060cf4e8475f93f3c8a634c3fc05b75eaf2f1cbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42bb9185d066277fd1c662f181dd3d98d74f982179b66658d8044bd8483a68a`

```dockerfile
```

-	Layers:
	-	`sha256:b1d298e7774fea3ebb0f378680fd9fe5a7227345f1e92d8a8f5bb7561b0230f9`  
		Last Modified: Tue, 04 Nov 2025 12:28:29 GMT  
		Size: 2.3 MB (2284976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f942b31474bfce92005254c89e81053a0b334f42328c9c7b3ebd0d56bd8c2606`  
		Last Modified: Tue, 04 Nov 2025 12:28:30 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:91b6b4da2fc6090374e0fda11e524d15864879c72ab8ea891305c6a5dcc6f8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79582515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7ede2b923eb0046c874d79a45ff044f0476e7c68dc32b7025c20e8b4e2e79e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 01:41:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 01:41:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:41:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 01:41:55 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 02:37:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 02:37:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 02:37:13 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 02:37:13 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 02:37:13 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 02:37:13 GMT
USER fluent
# Tue, 04 Nov 2025 02:37:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 02:37:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c83755afbe771e645a69fd11df0a60d6e7dd541fc57e5b0f1b0be4b2a0883`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 1.3 MB (1261429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c48599929aa6c7fb7bed5f82a13c0154ffb885b6f1e85e9f644b0767b1f70`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e552b7b884adedf291e273039ac04ca2d02aac2bf91d0790d8ed1417002926`  
		Last Modified: Tue, 04 Nov 2025 01:42:15 GMT  
		Size: 42.1 MB (42145432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35feb980ed30f707dcd311800ab0801ef0c69e411a8513d2d57f4e74def26a3`  
		Last Modified: Tue, 04 Nov 2025 01:42:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50f3b50e47c048e589ed069424290b2dadff117a2cfb2306543d6ea53432fdb`  
		Last Modified: Tue, 04 Nov 2025 02:37:29 GMT  
		Size: 6.0 MB (6030973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb7f246be820a9a7035411437ec82adb7b7e57751074a838dcb8b57853e218`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fee3af5dc401f90c63aff5571b43de11c5e287af015286ceac268d59823fb`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b82136c4c34e431e87e862f28be1d30faf08715c8265f07c8c6c3f747472b0`  
		Last Modified: Tue, 04 Nov 2025 02:37:28 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:12d71120b81b51551d597b9ce196c3ad25405bb7534bb306d9695e728dbe357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184e9b9694fc38927b46e669811d5a4188b127fdbfb32a2c12b823816eb472b3`

```dockerfile
```

-	Layers:
	-	`sha256:9af4c91c515dc26f2329814b50546b04473222e4ebe2c4a0c84c607529966896`  
		Last Modified: Tue, 04 Nov 2025 12:28:33 GMT  
		Size: 2.3 MB (2283836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff4bfd853e2bbafcd8a04cb7af0cf640464cbeddc807c9e1758691418aa7f0d`  
		Last Modified: Tue, 04 Nov 2025 12:28:34 GMT  
		Size: 21.2 KB (21231 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d59f8c6c6c48737bdee2b613c8be0b526308445a9ef7c51155188153a96409d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bfc4129e134cde48ec66678f6c9354593b1583a3c04b1206e3fc23244e5d6`
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
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 18 Nov 2025 05:23:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 18 Nov 2025 05:23:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 18 Nov 2025 05:23:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 18 Nov 2025 05:23:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 18 Nov 2025 05:23:00 GMT
USER fluent
# Tue, 18 Nov 2025 05:23:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 18 Nov 2025 05:23:00 GMT
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
	-	`sha256:e9c2c48995108a60e2fdb05fd46bf1c94df58eea647aa0374397956629776f6f`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 6.0 MB (6020036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100132077330bb34ce45d83a81f16cf3f6f7a1fa4b66721295830c751eed7d22`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e3fd12967d700f626d9eb0e4fec9d3f53b38855c87ae05e55f54878cccae2`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8738b2c1bc663caeb233d06fe7c070abcf20f451f96a98fdebaf1f68baf5f2d`  
		Last Modified: Tue, 18 Nov 2025 05:23:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ad02e8e57741432eb0abeeddeabc321bc1a3ae4e588add365adbed9dc60496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06acba6409fcb4f90a19dc1dcdf6f3b2f609d65530719626b23d86f3969bba41`

```dockerfile
```

-	Layers:
	-	`sha256:a510e27aac3d4a78bfa3dba5a3ce476be1c2e1e800f5dec0b75767889313dd59`  
		Last Modified: Tue, 18 Nov 2025 06:32:08 GMT  
		Size: 2.3 MB (2280746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d9037d52c68310672a681260a39b2504b5bd44113cfde3b5cd8f20a27e942`  
		Last Modified: Tue, 18 Nov 2025 06:32:09 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0394134b4106e1a322bc5bea388bc8ea50ff54a9ec059144495d0a36ce1895e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81071254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4416a657be5c504ac27d0c7cfc006b240f8440de7467c80ea69c3bc92deb14`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:16:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:30:02 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:30:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:30:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:30:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:30:05 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 19:58:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 19:58:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 19:58:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 19:58:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 19:58:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 19:58:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 19:58:41 GMT
USER fluent
# Tue, 04 Nov 2025 19:58:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 19:58:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7cafc9e521290ae17ae96071a62fa0ce9cc48a489bf957fdf15c09abb8a804`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 1.3 MB (1310384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74df3c614cf044979896d45fdbb3780600a0f2a6f1a699a70de10d0153e6928`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4312abe5d4cfc4eeefc5f2b09f01e9ba77dc6e592a8edc74346d8a87f2e45f28`  
		Last Modified: Tue, 04 Nov 2025 12:31:03 GMT  
		Size: 39.6 MB (39601068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf418f7fe1d0352a8b07d3730b4a8393da06df977da19a9696aee08825025762`  
		Last Modified: Tue, 04 Nov 2025 12:31:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091f8580ca0d0137a62e83860303b48b10b634f2bf8c18920dc53938f130c40`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 6.6 MB (6558759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718bc6b50d295b1fd485e209c3ff74421802ebc3cf2cef01b33cb7da8e34b56d`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd40aa235056c26c6f0ae37c8933e1bb288034d9df402cc18252f6469055634`  
		Last Modified: Tue, 04 Nov 2025 19:59:21 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7206d908d6189a487af234889268cf4d47da74c4477a00e4cfd36716b4da41`  
		Last Modified: Tue, 04 Nov 2025 19:59:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fae67ad3e796f6f0ecc8f62eb44739b84e730d986fd6ad5f24529f7d2d9f5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb05857bad1224261621c7abf7b6d6c484c2426724863ca259d07ec32a30073`

```dockerfile
```

-	Layers:
	-	`sha256:c37622be462407f9cc248533cbe5481f7f58bdfa498235b22b4fa1c6d44c5e02`  
		Last Modified: Tue, 04 Nov 2025 21:28:33 GMT  
		Size: 2.3 MB (2287099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb120fc15050a9d25f652c7c39a98e10d98d3dcaff6ec871e1c195547104024d`  
		Last Modified: Tue, 04 Nov 2025 21:28:34 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:1ba5ab678ead4498d917c4a7acd915ded9543f724cca2e527022ac6d159ca302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76838773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b70ec958c85adaa042b79d68f9db29879abdda7e2a6d46e6a9abd70dcff705`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:39:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 04 Nov 2025 12:46:16 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 04 Nov 2025 12:46:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 04 Nov 2025 12:46:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Nov 2025 12:46:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:46:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 04 Nov 2025 12:46:17 GMT
CMD ["irb"]
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Nov 2025 16:53:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Tue, 04 Nov 2025 16:53:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 04 Nov 2025 16:53:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Nov 2025 16:53:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 04 Nov 2025 16:53:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 04 Nov 2025 16:53:20 GMT
USER fluent
# Tue, 04 Nov 2025 16:53:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Nov 2025 16:53:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc87d0d125756f6f7207ff00dd475820f1f662c1490e4f973570b5313e17fb6`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 1.3 MB (1294636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7ffedbe0c72a7402c4c7ffa7ad05e05878b479406400dca12509798aee65e`  
		Last Modified: Tue, 04 Nov 2025 12:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f9a0ba0eb1a5da7986fb92d450451bc333572015535b1b763a366214e8b6b`  
		Last Modified: Tue, 04 Nov 2025 12:47:04 GMT  
		Size: 39.3 MB (39287395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46ca528085c3652d506f94d3950096f37aeec2bac6827ae4ff7383b0116b3a`  
		Last Modified: Tue, 04 Nov 2025 12:47:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa746dbbf4325707691bffabcca7d685a3cc3583cfe8ab8fbf04e6277f7aa0`  
		Last Modified: Tue, 04 Nov 2025 16:53:53 GMT  
		Size: 6.4 MB (6416957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8612a12f56f9dd86f9543a9f598cbf2d6a78e2b2142aa806819ba55ce2e4c`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9830c4ec73592c4e33e871e27ce42c0d59915736cb3509bce80fa989224d30d4`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5636653a1ba6f2e97b635e9f1431d02cdd51383519faadd8db32a4d63b5c29`  
		Last Modified: Tue, 04 Nov 2025 16:53:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc22a7b6537fcb04e3c6a4e56db9d883c06682e2e189a1b2234c412a224936fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee2879aa877fd3fc5831fc029db676d66d3e506782f7f836964f6b7b70dbbe2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d17eac27b3fcd0ccc656c80d3b5611487691fa4010b7bd570558181bcc774`  
		Last Modified: Tue, 04 Nov 2025 18:28:41 GMT  
		Size: 2.3 MB (2285009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327e0a83092a2b5e6b90c9f10c9f4cfd2fa1541fbcd2bbaa1a46c3b6057c9f1d`  
		Last Modified: Tue, 04 Nov 2025 18:28:42 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json
