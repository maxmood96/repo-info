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
$ docker pull fluentd@sha256:a3b979ff02198574027d393282b437824226abc01b560baf6cacaf1093dd346b
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
$ docker pull fluentd@sha256:98056e95ce560655b93bf9e3add0b525a759f81c075ffe847a2e1244399e2c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79241950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc77db10b97ffbddc69d46dc9a79c1d65c3d3b1b8b1425d88d6dad488bc40c3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:17:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:17:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:17:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:17:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ac34359c677603e047bdcaccffb13936db90415cd5425e19a772e106c2321`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 1.3 MB (1279325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dfdf3108059b075552a568a23ff473640e2daf0955ed48e9ddc91233660d9`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40877f1c75ec092931fd9e55b6bbe54e219d4db9a19d156104759811def3d73`  
		Last Modified: Wed, 11 Mar 2026 18:40:09 GMT  
		Size: 42.1 MB (42127122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de739fed639776f972632f3ffdfa182e9b7e5757a07c23eee68909575e9d3b`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ac0f133320bc335da9c95abc1dc4fc31b1933c84da67904793260ceada3b9`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 6.1 MB (6054470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc056f0ff48fcdc7014eea0e3415dfe68564b64192e6493aca5ddd505fbf858`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6e732aa46723bbd4ddf6d1e4f1fd258238f597500bcea984063c7789bed32`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff54ee029054b8e813346a65f20505870f97e351cd87d287bcb416058f0f2c`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:410c6d0ea78960b05d776c327a23d2d09d3585ba4560823b03770094bb53c971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e92bf16648cc1cf6d10605fc07d3a0f3bb3ad36e8c389599796f55435f4830`

```dockerfile
```

-	Layers:
	-	`sha256:bd3d8714193e4415b79965a1e0e5a20fe390d651058347f64018666ce7535075`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 2.3 MB (2281602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e41ae761368bf1302b51b81472be2f702e1b2a170c85b8905b96ea19f5440d`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:68a5254df265367ba3240ed09837659996b73d423c8aa117d3afe7dc691ae5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73093351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bb0bb4b651d7ff5b5e3b486dd363d17f4628e86a96a084ed8716ae03c888e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:35 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6321774249b9f1f6a028db4ffc2b11915c3e980c9732ee9f530f5c3569bd84`  
		Last Modified: Wed, 11 Mar 2026 18:39:27 GMT  
		Size: 1.3 MB (1262989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec27c1bcf4ae4bc343b5a1cea6d4f9c4e6aa745f051ef2c211f149803598f07`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab58b7d03dbd70019e0b0a24d6fa5f28bc2457a7d52426c4e9de48b6b0d0caa`  
		Last Modified: Wed, 11 Mar 2026 18:39:28 GMT  
		Size: 37.9 MB (37924091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3693cee0228af01605d48961da617a4156cb2151ef75ea795fd0dc33fbd7af3`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4192a4414efc21cb382168c931e6b4c348b07644fe861cd8d92c0f17ca7fc4`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 6.0 MB (5956263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e272f35dfe8731a3dfe2f513f97317a783a0d1a21c190219a11bbf45007d016`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f608bf1730643f7b338277cb73a19e443c631440ffab0bedacd404a1ccd6c7`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7de86d98e35e01f38c2a2dca1dc9e12f54cd6a9948b29e4d5f5596eb580d7e`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:875dcddf186d6a7c1ca83ad12cb280aabbff897a4f9c31aa76f7a2b36ba460af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284fbaf5dab49d5e1186cc667d05d23fd8750734fbef5643a9881221e5741e83`

```dockerfile
```

-	Layers:
	-	`sha256:2e1094a84d67cf8a9b77ae9560dbcced987c8f836ce914990a1ae6b3878cb8fe`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 2.3 MB (2284573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae864229389ba2f91d720ffff75c0a266ee621541890381cfe2a1506af2c913`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9744668bd9d7b175198981686ccd087fc0e2d54fcd4ae52a9508587f7ef56299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70957474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356c070c0ae8f1d5a86f18e6159c992e2090afc05eb80e73ecbafa4a44b3d663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:48 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0209b5ab14c5cc59c579ccd641d0afbe46c56b33a0bd99ad4e55993acfe06`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 1.2 MB (1236647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2b9c4fdd125bdaeaba20b679baaef269fbc6a6f45ae5171de3a5892623dca`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec177ea5e920d6d3a3bb9bdd4d79fea0c9d744b56c92bd8e64612a09948c6d5`  
		Last Modified: Wed, 11 Mar 2026 18:39:49 GMT  
		Size: 37.8 MB (37780192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b28d7b6b0a91bcd005637f2b7561587b89331fc0472d206b8ea8eec240756d`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423d30686507d592e38227ec924f9bd97662a25fdee7f775f3ffd1d4e7eba2d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 5.7 MB (5724488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c126699186495e24d6314913ed99194bfa184bbf7cda08cf7c85adf96d14078`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397cb9490c05559548d85714db1497d466b328d2a895de8c91c2efc5fb6667e9`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7798f2052bd0ab151a24fa244236b305efe966fa5dfe7f19f566e9fcd39665`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fbb290e1c70ac79ac172f264f7551797598697d56f34697ad4dd29dabeaf3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088bcf5bdb793831a793b6ef968d64a2f1a3c69c471b16aa1c5a98a765b89b5b`

```dockerfile
```

-	Layers:
	-	`sha256:b4bb1b78d1d4bb005109b6fac820ab004d83eec9e7a9979eef511d48e3bab666`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 2.3 MB (2283014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51aa187f24eca0e5cf6d11396dc12cec04d2728f4f16cab0c06f130f7c9db1d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4c47e798fb7a41e99b3816b96f1622ec0f8bf0b027f9ea5d3950675c965e49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0b1ee3cdff3e88ace68e382bcc71fa2110e17eb6dc41236baa40c2c882770a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bffa5cd1691dc6366ce11599d060f6c5ad180c0ad4d6810c1ac498466519d`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 1.3 MB (1261281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca28f67fe6a1ecf02ad7ce4905c032d859938153906fd15be595d38309d2e0e`  
		Last Modified: Wed, 11 Mar 2026 18:39:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b0ec96ddb91dfec10e0899ce1e8bb136293dcd72e24f2bb4f5d196126a848`  
		Last Modified: Wed, 11 Mar 2026 18:39:54 GMT  
		Size: 42.1 MB (42077901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d968e78d8934ffa4723337b3ce8e4f69ac350fe6d45486190e7eb8221faf41`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef55bac5c015d80d282bc0c7aad04233af0b956b0d37da47f686e9cbe63840d`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 6.0 MB (6043926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480f56a9c12d248c8faff32f2ee2976018eb52120ff19c05f5010301345e007`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8081c5f39e3acfcf03bb30fe7dcf87d0adf7c449b14ce4c248c420a416609cb`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221204832776264f1aa4eaef5974dcb354b7c2b77001c9f10a131d1b4939ef5b`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c1d8345d82bfa035c5fa41f17001be477894b389541645a823aa75aa72c6ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5012e26563df9e334d747dc8bebabd27f94eb87d278a38d6a292183f6b473ce`

```dockerfile
```

-	Layers:
	-	`sha256:62c7cd819c5dd97ff517bb3baaab1da5a78d7fbf161de33ec9e96a142ab39a89`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 2.3 MB (2281874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801a09bb3467020196a76bc15ad49a4568bd3079f387e4a563934d3f562014e4`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:a34f4faef125d2c1c0b7bd866ca0e3132e10cbc6cd2656b7556a2f267618a1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd2a7233616b14025152fae14adbf8d1fc10e410271edbcbf38eeea4d8f413`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:02 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:02 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:02 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88f57d04c7cfe5bb1217bad3e3ff16c30aea89aaade4ec661e53853315a02b`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 1.3 MB (1287310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447bad7b66208f8e935f58d734a53f366f3d6017c5a21abe67c4dd2540f77efb`  
		Last Modified: Wed, 11 Mar 2026 18:31:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dd3c17eee9b3bf39cca9d43f8ff495a7c75199811b65bda5f566afbe968fe`  
		Last Modified: Wed, 11 Mar 2026 18:31:56 GMT  
		Size: 37.7 MB (37661725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00ce345593bb8166503f9a71eeb0eec086b76f9b8ee5d85378d6ce7384165d`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d889071b4c31131058eb1717f21630ae829bf20236346853191378472378`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 6.0 MB (6025573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd2386539996dd7ecbb76d8338b4e6ba89be42afd48f6e7f4ee160816220458`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e088c0c3706d7a1de6a2a99084988cb91ba507a308c257bb4e2d242023049df`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13c7afe2833b7e6653f6d520c277980f2e7a7621d992f45dc898511516b52c`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:2f589f391f45d80df48ea7b5a8d3ba4a2f836763858f99aa95b3ab3e934cf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f93cc26b17337c0c4f8bdd44ea80516d4fb2bb69783f1696fbf270c18371647`

```dockerfile
```

-	Layers:
	-	`sha256:ba093f17127866de97e95fda615ecbac913309fe75b394d315796d3e2ca85a12`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 2.3 MB (2278790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b5868101a72b0da8c025457d3c4d4e1e55a5296194e5614c043c2c4593900f`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de8d3ad6ce1849bf7b5f28006b9212783ef94e4561909d461485a8fc1d8257ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81019590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52803c668efdfed3a0b2398ea8ef2d6dfe238fc97d6e040701d543478b16aa51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:45:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:45:49 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:22:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:22:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:22:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:22:18 GMT
USER fluent
# Wed, 11 Mar 2026 19:22:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:22:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bba5358e3f378909e4c0a9cb9af69228f3108fd67a587461fccd3158cb37a6`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 1.3 MB (1309516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bde25b75aac9ba75f7885fbf7286727e870ee78b380c72bc612e409b3f55ce`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928678f951f229519de045ee3851c120dd40d5a36fe1846396e5695cfd5f76c`  
		Last Modified: Wed, 11 Mar 2026 18:46:07 GMT  
		Size: 39.5 MB (39531725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b362d31236d551dffe973f43a7c056cf3d2c5be3d482402a299b46c47d7bbde`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca75c809c185b8b9b3af8851c647e673b0c586e1a1b9afc4085e682cdda7a10`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 6.6 MB (6575733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf00919f179c5e952b990fdaee3167ae0855465c1648e9d6ce0dbb6254aa0c4`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b58f73d83f66b53787162bd9f95f7898ac610e24cda3db51a3bd3222d7806`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc55a1d404e92beb7cc18af679e3b12fd3567c6e4e86adda49137e2f24657aa7`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:e134ec73a0dfba5d8cb13f30e4967ab90a3cbccb35389ee43f15b5e8b9d994a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777a754e5615e3f977cb9a52c9c13ac48bd2fde7739a3cec265f9fcd8900344`

```dockerfile
```

-	Layers:
	-	`sha256:895467fd95e7f9047a1b753596a06673f51c2442449f6a0ea05847c089380b8c`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 2.3 MB (2285137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebe8cc4e199aa617ed31aabf514d168691d23c17158c4343019e5025a4f5c47`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:15272769816a339589731725f28014f3cf73e0416f3f0d3afd2ac0dbfb6a95b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3375b66a23ddd0134dfa3c5f5af79b3e2c54f6f5cbcf892481165aa944ff24c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:44 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2330c467e1931fe73b76bbfce21eb00bbeb1b3408d0f700032ddcb64bb358b`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 1.3 MB (1294488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342513ff2afeeee15c2a6131bc1f9b6bda0e30048d575aa73c13abe3642f4ac4`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096e51e12f56f8972511878c2bdd53785b95467ddc2431a3ed08203e984dfb2`  
		Last Modified: Wed, 11 Mar 2026 18:33:47 GMT  
		Size: 39.2 MB (39205804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c44d6373d7f22f1af2eea10934cea9eef1965e287d8d54f607bda53e16f41`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059721229294da070222585983b257cd6ca81f01a46688fb93366f12f193c09`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 6.4 MB (6429931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff45129a091c48baccc63e67d8f470f5b5c610992ac341d2ca285e35ef3965`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf75ab18f67fb4f9382c309c081e6dbc0fcc15822f4b2fbc758b6db88843aec`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9056a71b599985194f6a6956b6a3879d3c1dd3eb967f2daefff034e1c312f8`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:71504d474cab676e050e9baa575e5eb76234b6a52da2e426ba13b5bd4a2d05ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a78d1b92735b8fbf7a02be684de548f50814027e99dce875d8f8a819f2cc9`

```dockerfile
```

-	Layers:
	-	`sha256:f02789c7eaf625e4c19a111f65e5d6fbe7d3cc7f4fdb8f430a2480298891066d`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 2.3 MB (2283047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a433fca29ae7cbd3a34d6df5ae84cc11f5dbda5e3bb534023f73842d62a6bb19`  
		Last Modified: Wed, 11 Mar 2026 19:15:57 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:43db27868f83ef136effa526477ba962ca7da31efaa3537ddcf30605be700df0
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
$ docker pull fluentd@sha256:4771f99b3a0503b5f8ea0aebf183750b9ce43ed3a05ce8781531da406a3a9b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82052691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6913e6da5ea421435e3eda6ae6f6d8538532a259063eb31d0b0d52cd3a68563e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:22:23 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:22:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:23 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df150c11f2d58174c3aae4f604576f28b185b28a616fe846715511ed0f352827`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 3.5 MB (3510182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec15dd55a363b0c43f66110f30b067c2de0afae2c49fe4e1b69b4ab7991116`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4928b0a24e7aecbedd132a84cade78772c1b4bbfcc2e6092a03853a9dac3a3`  
		Last Modified: Tue, 24 Feb 2026 19:52:03 GMT  
		Size: 36.0 MB (36010873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a29a156687ac9ec641538d5375f0856632e3417fcad442c59ce5ecad97014d`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e29c7a5c16cb97f5cb44bbf2b0a3880e500b981ac81d6136ac0d6f397198095`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 14.3 MB (14292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014efb356efee47753666b4ffdbe57af7f6d225b0276c700a1e1d028902a8c9`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae20c2ec95b5fd71a79cec01786d4b3ab525face8e909732bfb02e9db534b32`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8ecfe875da7355a981424f702e7ab999d742571212d4871f58d0b15a0d9f92`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:27fa70ae9e522f092017fcfa2d46d520511cc6a0c58547977cef315d61498d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778a0710dd9381f25082d5506f5b4929230c561b9c6cb4641df7e844c5fdc5b`

```dockerfile
```

-	Layers:
	-	`sha256:f0ddd225c0b68c934863f47ef5b1d58a2b491b20f5724431a4fc6ecfca3f7d1e`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae75545ce8a06fb0cf663745b8c622999210bac34e6b381ba033544a9d379c4`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 21.1 KB (21071 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d2d8eb7b5d6b6ee0824a8eac544b9ec87f8b2a559cca755e4a5d9eaa5c227661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75450577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84266c09879b21def70ebcba34f1f323fb275b9d977f060dfe6ad5c4f4eb23d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:54:41 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:54:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:41 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3eecc313abaf89f694406c0f1fcf4bb7ae74557455bf5d9df9661bd30185e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 3.1 MB (3081092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de71683607fd2d40421fde9555243a10bc991cc34665772f5076f51820c98e37`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362d4d1eed694fdbcec1d943ce7b1e98cbb2c1ad48d3e647ba1a09bf1b8244e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 32.3 MB (32331019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1afd6aa174dc2b046476cf27e76cee1cafda009dffa6906571cdaa4d530a52`  
		Last Modified: Tue, 24 Feb 2026 20:42:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52a17ce755df3d0c91f11aa754ef1c72396853ecaa5630242702b0e627ae78a`  
		Last Modified: Tue, 24 Feb 2026 21:54:50 GMT  
		Size: 14.3 MB (14270433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570ac50ead433b23781f3e31a9ab171b183e0294710a24bf4edf3f66fd403b6`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f070a174fbddbfe1df03c2269983985072081cc6500426a3e8964fca59c08f`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d553391c9fed1836291de7c8f673b8ad6eeda4af2d7f43d2ef52b170e9ef49e`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9b15b7fd80216027ccf3376da5c43355e7aab18a48c94402cb0741eef06e0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59b7dda6c296f596a2198d566310724eb1706c0563d1d980abea0dee67a308e`

```dockerfile
```

-	Layers:
	-	`sha256:f545739d6026404686095c3900d847a818ea4e5dc0c7bfb545962c528aa45a03`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccd05a58686bab81efdd0be5560999d58c57ba74f5bca494348b2c435ba5a37`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 21.1 KB (21148 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:51332f4710759ac1bcd42f09508fed0d458d6626321adc4b5b5e7ce7000d9e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4da8dd161bec02c3770d8da8c0bab3cb26ca4d512bb21aefdf93cde6736b69f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:10:22 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 22:00:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181815e651be48f7e0fbc65e79272338249cc4825fc8fb8d39e40e6206f8dc88`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 2.9 MB (2913768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07adaf3cb294573dec3eaf97db055d58921f4b821cab9877be5cb40a718a134`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce340f292387a0bc0b908fe2b2b1b642907fb498c28a05e7fc9b06b3d1c024`  
		Last Modified: Tue, 24 Feb 2026 21:10:31 GMT  
		Size: 32.2 MB (32168041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99bc1ac1583e8e092909d0d3c2c9219be66af29ccf3f8047eabfcd104191f86`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c493bdbc8c593f0f92d04ef24d0fb241bc89253415d11b73ae7376e631bbe1d`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 14.2 MB (14201729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d8fe43c9f1949bc70ba61c37b1f6dfba74b3dadef3bfc3276c06393669629`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef48f0f4f167872496d02434df4f78ffc601fd9b3cfd0e5084a38dcee17dfcd5`  
		Last Modified: Tue, 24 Feb 2026 22:01:02 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3a132251f9a5ebf77c40c2bb76e5f4a775673d99efec076c17409bb0a027af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fccab6e8e77f90628b336eda8b365a115aede522ccf210a7df18f4a0993bc`

```dockerfile
```

-	Layers:
	-	`sha256:ef83f68dbae07b06ed5be279e4fcd2b54788396ac6a853dbf4ce9f79b021abd6`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f20d0220a8d7d02f0ce981d622fb8293876536f21dbb822a520ce1954f57bb4`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7040043d4a50aa3e045ec0c0bf1e59ee80554641fd45ad8db1a50a709d8e9baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15440eb9f2c5a93491df065cf4a69a61d0cb03cfeeecfbfc302978338c95464`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:38:25 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:38:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:25 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:25 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:25 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6a207c45083e2aa3cda7da1a0180e6755cd4bb26c170a1f3760fe5bb4d45c`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 3.3 MB (3341511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c113a5f4448070219ca58e995aaa6d5837eb674822494cd99ada8e20e5ae657a`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28198b8b91be8fbf9abc3de9a3f968e48296bb9fbec2c8191bc44e151b9c58dc`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 35.9 MB (35911763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff80bd722a6c168e8aaac8bd77c49137a2803149ddb3db43d6daa65c02328e`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be27fcae1cae3e6ea9f5c8ba393cf3f95c332a14527581a06c7092610f2b57`  
		Last Modified: Tue, 24 Feb 2026 21:38:38 GMT  
		Size: 14.3 MB (14298864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7ce0476c9336412c661397d95033d94258000afa9072a7c76500c9aa3850d4`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efee239239a544a65959d9d868adca407f05a9c825678de07fd9ebed726cb4a`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98943c28255aace405a4febfa3e5481226b13e1377d811ed0b7d5cc50ad7d6`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:80f98fd9ff202a89bbce13ae8f00cf91a89ab9756f9f36d892f3c3b6ba08b1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3086a2fe2c83218e8388b72dbbd990614f326a3df0ca4e50b53bbe830e81ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1729083e144550a50e5125994d665085a0511312e4eb74a87c3f0226c21262d`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0394b9abb40256f20fb5740c00032f1216c1c590288ebdee67e9cb854e375f`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5c4f6ffad93fbad17d6aa131216428e1c15644a4903cdb41f62536a4428fd296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78983951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207f915b460d5665d0a02b673c850e5e842591604a447db314e19b0d580bba2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:50:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:14:43 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:14:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:43 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:43 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc97e1b8827deb66c8f55b63aa24a717166c23c116bfd32fbd210f382acecdf`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 3.5 MB (3512925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17762cd40b5013880f2dc74d7021819b98739a6250505c6d6bad05beb0baba3`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57afe41774a91d5bf4827fd241077ca7fd3aa50bbe5c7d27d3487ee987de1380`  
		Last Modified: Tue, 24 Feb 2026 19:52:17 GMT  
		Size: 32.2 MB (32163465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e92ca4f16ad2c4f2c1e21f71b07ebc1a54c39ecf03d4123e2195457b6d7a4f5`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f26d050631b1598d9563e0ebc9413bba3819d6d8800733ed659015cee7c95`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 14.1 MB (14083462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab423f0cf0e00bb38746a54ac895cc370be34077dba1ebd5dac64fdd14eda`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccb2f2eba9b30c0067b2d308ca5a1430a1861e6fa16743fb3b8bb1198917c83`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12c5a6f6001ec1271796c5d8756d429f533928dd1339bc921c2ca0f8f2e767`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ed16d2be1481d029c17cd7582c6d7d5216d4bd26615e300f655ddd8f00bfdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820d87dc396a6dfd3ad9d5335e7e95d50587dce35b25f781b48f1b3b430e4cc`

```dockerfile
```

-	Layers:
	-	`sha256:44c55ddf3bc8749a5defb8ecbf589437309c16ecebdc474d4195e0f604821ce0`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e74b71ed7da334df84404550da95607f6a249bd0c7be0718ed69c1a594bfbe`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 21.0 KB (21048 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4726e436b8dbe953854158459856a9f367571c9ad7f7ddf953459f6139e9987d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84324188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600ab2ea184685004b946827ca3d0b50ad3ba5415f375d8ee12f539e59f8e205`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 01:12:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:35:32 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:35:32 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 25 Feb 2026 01:35:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 25 Feb 2026 01:35:32 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 25 Feb 2026 01:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:35:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:35:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:35:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:35:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:35:33 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 05:48:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 05:48:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 25 Feb 2026 05:48:35 GMT
ENV TINI_VERSION=0.18.0
# Wed, 25 Feb 2026 05:48:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 05:48:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 05:48:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 05:48:36 GMT
USER fluent
# Wed, 25 Feb 2026 05:48:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 05:48:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1172197821b9eefd61a069d7a50a0bc461521531f0dbbeb1ab75a50ace0baa`  
		Last Modified: Wed, 25 Feb 2026 01:18:53 GMT  
		Size: 3.7 MB (3710810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1821109e0515ba6c920a36de6a644db2867ab56a6ba097d9d58836299f3a60`  
		Last Modified: Wed, 25 Feb 2026 01:18:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d921933e276a7bc487ddd10b2e0c803b78d7c22c1aed74a2f8dd66f8cc486c24`  
		Last Modified: Wed, 25 Feb 2026 01:35:53 GMT  
		Size: 33.8 MB (33835852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e44eb68ea620bc100708dbfadcd1fd88a32545069458a36a79b1c1576caa9e7`  
		Last Modified: Wed, 25 Feb 2026 01:35:52 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96be5264b51fcd424b3d4838a08f161aae0d3de24b9ad58cef97b8a16338304`  
		Last Modified: Wed, 25 Feb 2026 05:48:58 GMT  
		Size: 14.7 MB (14696796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d3a24d9485e167f2c7d6d7a223847d333ca9d28c8c710bed00baf9e01c3b53`  
		Last Modified: Wed, 25 Feb 2026 05:48:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5a639329bbc4665d2a795c4e613d1bacd128575424c11775eccffbedfbe614`  
		Last Modified: Wed, 25 Feb 2026 05:48:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f402dc1cff9c82a3f0ddc3170a3b7f0048fda95cd8bc36e12f1b2776e9d30`  
		Last Modified: Wed, 25 Feb 2026 05:48:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:26ecebcb501bd77e320299f53c454b1fa71ded91c760f18a7a57b307a590cb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe17f8ea063134b3f66c51f892bc35b23d25ed0757fbdf82e9f165067aebfb6`

```dockerfile
```

-	Layers:
	-	`sha256:59f6b93f01b3715375164b79f6df59754d6e0902ec6a67878baa72e085964b38`  
		Last Modified: Wed, 25 Feb 2026 05:48:58 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54c874829b14d189a6001a5619763dda67a8a224b0685c5f7272e3b943c419a`  
		Last Modified: Wed, 25 Feb 2026 05:48:57 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:a39bcfa77efc7af7c937a08d332b07eb6ffee006aaafb9cd9b2d3c79f432cc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77599356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9df9d9b17e23c2dac02ed0c379d82b513e8b55c9e1fbe660cf61cad7cda9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 22:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 23:07:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:07:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 23:07:33 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 25 Feb 2026 02:39:21 GMT
ENV TINI_VERSION=0.18.0
# Wed, 25 Feb 2026 02:39:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:23 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee0a8590e769ec84c9c999b84ef7c697884603dfeac17e2f74cb19194158987`  
		Last Modified: Tue, 24 Feb 2026 23:02:46 GMT  
		Size: 3.2 MB (3171209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba25f0557aafc3759d760486d757d65a9bb3e1c108c3458785dc2ff39fc676f`  
		Last Modified: Tue, 24 Feb 2026 23:02:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8f23b843a21ce3f239a4d6af280bf2729dc51d0ac0483462479fae094340c`  
		Last Modified: Tue, 24 Feb 2026 23:07:52 GMT  
		Size: 33.1 MB (33104236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf4ff6bfa8f17cec32e84126297cd2c142213d9e37f0d2ffd9e7795450567b1`  
		Last Modified: Tue, 24 Feb 2026 23:07:50 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be13b0e8917723a0af24cbc141920b530c9a24cbe9d72925549598334842e639`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 14.4 MB (14429986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b0786c75adf02326337327216b324d581bb04e65603b8fc1dbd4a43135884`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08315f43215c0225ec306a8a7c05a553aeb6b2d2284697ad375315c7700738c0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84550c0ddc77f8b63a983e57aadb590d16013d0a2b85a5d3cbe7dc9c29ec81ca`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9df0560ccf9cc0eb9a0040a1553bbd954239feadbac3cade9b4300aa6cc969ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1e46b02eaf9f954b5ac4771b7efae352a149c78ea63c9a8cbbb716083e91da`

```dockerfile
```

-	Layers:
	-	`sha256:50f8c4edc2f854be02126e76fddc0f06a70ce49cd96b71d70cf1ce2855500131`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18427afb6fd0aaec0ae12fd27cdd134735954f8ad9f215bec007f6742693b4f0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:43db27868f83ef136effa526477ba962ca7da31efaa3537ddcf30605be700df0
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
$ docker pull fluentd@sha256:4771f99b3a0503b5f8ea0aebf183750b9ce43ed3a05ce8781531da406a3a9b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82052691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6913e6da5ea421435e3eda6ae6f6d8538532a259063eb31d0b0d52cd3a68563e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:22:23 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:22:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:23 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df150c11f2d58174c3aae4f604576f28b185b28a616fe846715511ed0f352827`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 3.5 MB (3510182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec15dd55a363b0c43f66110f30b067c2de0afae2c49fe4e1b69b4ab7991116`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4928b0a24e7aecbedd132a84cade78772c1b4bbfcc2e6092a03853a9dac3a3`  
		Last Modified: Tue, 24 Feb 2026 19:52:03 GMT  
		Size: 36.0 MB (36010873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a29a156687ac9ec641538d5375f0856632e3417fcad442c59ce5ecad97014d`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e29c7a5c16cb97f5cb44bbf2b0a3880e500b981ac81d6136ac0d6f397198095`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 14.3 MB (14292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014efb356efee47753666b4ffdbe57af7f6d225b0276c700a1e1d028902a8c9`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae20c2ec95b5fd71a79cec01786d4b3ab525face8e909732bfb02e9db534b32`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8ecfe875da7355a981424f702e7ab999d742571212d4871f58d0b15a0d9f92`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:27fa70ae9e522f092017fcfa2d46d520511cc6a0c58547977cef315d61498d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778a0710dd9381f25082d5506f5b4929230c561b9c6cb4641df7e844c5fdc5b`

```dockerfile
```

-	Layers:
	-	`sha256:f0ddd225c0b68c934863f47ef5b1d58a2b491b20f5724431a4fc6ecfca3f7d1e`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae75545ce8a06fb0cf663745b8c622999210bac34e6b381ba033544a9d379c4`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 21.1 KB (21071 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d2d8eb7b5d6b6ee0824a8eac544b9ec87f8b2a559cca755e4a5d9eaa5c227661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75450577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84266c09879b21def70ebcba34f1f323fb275b9d977f060dfe6ad5c4f4eb23d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:54:41 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:54:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:41 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3eecc313abaf89f694406c0f1fcf4bb7ae74557455bf5d9df9661bd30185e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 3.1 MB (3081092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de71683607fd2d40421fde9555243a10bc991cc34665772f5076f51820c98e37`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362d4d1eed694fdbcec1d943ce7b1e98cbb2c1ad48d3e647ba1a09bf1b8244e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 32.3 MB (32331019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1afd6aa174dc2b046476cf27e76cee1cafda009dffa6906571cdaa4d530a52`  
		Last Modified: Tue, 24 Feb 2026 20:42:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52a17ce755df3d0c91f11aa754ef1c72396853ecaa5630242702b0e627ae78a`  
		Last Modified: Tue, 24 Feb 2026 21:54:50 GMT  
		Size: 14.3 MB (14270433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570ac50ead433b23781f3e31a9ab171b183e0294710a24bf4edf3f66fd403b6`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f070a174fbddbfe1df03c2269983985072081cc6500426a3e8964fca59c08f`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d553391c9fed1836291de7c8f673b8ad6eeda4af2d7f43d2ef52b170e9ef49e`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9b15b7fd80216027ccf3376da5c43355e7aab18a48c94402cb0741eef06e0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59b7dda6c296f596a2198d566310724eb1706c0563d1d980abea0dee67a308e`

```dockerfile
```

-	Layers:
	-	`sha256:f545739d6026404686095c3900d847a818ea4e5dc0c7bfb545962c528aa45a03`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccd05a58686bab81efdd0be5560999d58c57ba74f5bca494348b2c435ba5a37`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 21.1 KB (21148 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:51332f4710759ac1bcd42f09508fed0d458d6626321adc4b5b5e7ce7000d9e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4da8dd161bec02c3770d8da8c0bab3cb26ca4d512bb21aefdf93cde6736b69f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:10:22 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 22:00:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181815e651be48f7e0fbc65e79272338249cc4825fc8fb8d39e40e6206f8dc88`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 2.9 MB (2913768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07adaf3cb294573dec3eaf97db055d58921f4b821cab9877be5cb40a718a134`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce340f292387a0bc0b908fe2b2b1b642907fb498c28a05e7fc9b06b3d1c024`  
		Last Modified: Tue, 24 Feb 2026 21:10:31 GMT  
		Size: 32.2 MB (32168041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99bc1ac1583e8e092909d0d3c2c9219be66af29ccf3f8047eabfcd104191f86`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c493bdbc8c593f0f92d04ef24d0fb241bc89253415d11b73ae7376e631bbe1d`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 14.2 MB (14201729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d8fe43c9f1949bc70ba61c37b1f6dfba74b3dadef3bfc3276c06393669629`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef48f0f4f167872496d02434df4f78ffc601fd9b3cfd0e5084a38dcee17dfcd5`  
		Last Modified: Tue, 24 Feb 2026 22:01:02 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3a132251f9a5ebf77c40c2bb76e5f4a775673d99efec076c17409bb0a027af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fccab6e8e77f90628b336eda8b365a115aede522ccf210a7df18f4a0993bc`

```dockerfile
```

-	Layers:
	-	`sha256:ef83f68dbae07b06ed5be279e4fcd2b54788396ac6a853dbf4ce9f79b021abd6`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f20d0220a8d7d02f0ce981d622fb8293876536f21dbb822a520ce1954f57bb4`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7040043d4a50aa3e045ec0c0bf1e59ee80554641fd45ad8db1a50a709d8e9baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15440eb9f2c5a93491df065cf4a69a61d0cb03cfeeecfbfc302978338c95464`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:38:25 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:38:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:25 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:25 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:25 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6a207c45083e2aa3cda7da1a0180e6755cd4bb26c170a1f3760fe5bb4d45c`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 3.3 MB (3341511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c113a5f4448070219ca58e995aaa6d5837eb674822494cd99ada8e20e5ae657a`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28198b8b91be8fbf9abc3de9a3f968e48296bb9fbec2c8191bc44e151b9c58dc`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 35.9 MB (35911763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff80bd722a6c168e8aaac8bd77c49137a2803149ddb3db43d6daa65c02328e`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be27fcae1cae3e6ea9f5c8ba393cf3f95c332a14527581a06c7092610f2b57`  
		Last Modified: Tue, 24 Feb 2026 21:38:38 GMT  
		Size: 14.3 MB (14298864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7ce0476c9336412c661397d95033d94258000afa9072a7c76500c9aa3850d4`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efee239239a544a65959d9d868adca407f05a9c825678de07fd9ebed726cb4a`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98943c28255aace405a4febfa3e5481226b13e1377d811ed0b7d5cc50ad7d6`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:80f98fd9ff202a89bbce13ae8f00cf91a89ab9756f9f36d892f3c3b6ba08b1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3086a2fe2c83218e8388b72dbbd990614f326a3df0ca4e50b53bbe830e81ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1729083e144550a50e5125994d665085a0511312e4eb74a87c3f0226c21262d`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0394b9abb40256f20fb5740c00032f1216c1c590288ebdee67e9cb854e375f`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5c4f6ffad93fbad17d6aa131216428e1c15644a4903cdb41f62536a4428fd296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78983951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207f915b460d5665d0a02b673c850e5e842591604a447db314e19b0d580bba2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:50:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:14:43 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:14:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:43 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:43 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc97e1b8827deb66c8f55b63aa24a717166c23c116bfd32fbd210f382acecdf`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 3.5 MB (3512925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17762cd40b5013880f2dc74d7021819b98739a6250505c6d6bad05beb0baba3`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57afe41774a91d5bf4827fd241077ca7fd3aa50bbe5c7d27d3487ee987de1380`  
		Last Modified: Tue, 24 Feb 2026 19:52:17 GMT  
		Size: 32.2 MB (32163465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e92ca4f16ad2c4f2c1e21f71b07ebc1a54c39ecf03d4123e2195457b6d7a4f5`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f26d050631b1598d9563e0ebc9413bba3819d6d8800733ed659015cee7c95`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 14.1 MB (14083462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab423f0cf0e00bb38746a54ac895cc370be34077dba1ebd5dac64fdd14eda`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccb2f2eba9b30c0067b2d308ca5a1430a1861e6fa16743fb3b8bb1198917c83`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12c5a6f6001ec1271796c5d8756d429f533928dd1339bc921c2ca0f8f2e767`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ed16d2be1481d029c17cd7582c6d7d5216d4bd26615e300f655ddd8f00bfdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820d87dc396a6dfd3ad9d5335e7e95d50587dce35b25f781b48f1b3b430e4cc`

```dockerfile
```

-	Layers:
	-	`sha256:44c55ddf3bc8749a5defb8ecbf589437309c16ecebdc474d4195e0f604821ce0`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e74b71ed7da334df84404550da95607f6a249bd0c7be0718ed69c1a594bfbe`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 21.0 KB (21048 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4726e436b8dbe953854158459856a9f367571c9ad7f7ddf953459f6139e9987d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84324188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600ab2ea184685004b946827ca3d0b50ad3ba5415f375d8ee12f539e59f8e205`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 01:12:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:35:32 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:35:32 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 25 Feb 2026 01:35:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 25 Feb 2026 01:35:32 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 25 Feb 2026 01:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:35:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:35:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:35:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:35:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:35:33 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 05:48:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 05:48:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 25 Feb 2026 05:48:35 GMT
ENV TINI_VERSION=0.18.0
# Wed, 25 Feb 2026 05:48:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 05:48:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 05:48:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 05:48:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 05:48:36 GMT
USER fluent
# Wed, 25 Feb 2026 05:48:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 05:48:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1172197821b9eefd61a069d7a50a0bc461521531f0dbbeb1ab75a50ace0baa`  
		Last Modified: Wed, 25 Feb 2026 01:18:53 GMT  
		Size: 3.7 MB (3710810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1821109e0515ba6c920a36de6a644db2867ab56a6ba097d9d58836299f3a60`  
		Last Modified: Wed, 25 Feb 2026 01:18:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d921933e276a7bc487ddd10b2e0c803b78d7c22c1aed74a2f8dd66f8cc486c24`  
		Last Modified: Wed, 25 Feb 2026 01:35:53 GMT  
		Size: 33.8 MB (33835852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e44eb68ea620bc100708dbfadcd1fd88a32545069458a36a79b1c1576caa9e7`  
		Last Modified: Wed, 25 Feb 2026 01:35:52 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96be5264b51fcd424b3d4838a08f161aae0d3de24b9ad58cef97b8a16338304`  
		Last Modified: Wed, 25 Feb 2026 05:48:58 GMT  
		Size: 14.7 MB (14696796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d3a24d9485e167f2c7d6d7a223847d333ca9d28c8c710bed00baf9e01c3b53`  
		Last Modified: Wed, 25 Feb 2026 05:48:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5a639329bbc4665d2a795c4e613d1bacd128575424c11775eccffbedfbe614`  
		Last Modified: Wed, 25 Feb 2026 05:48:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f402dc1cff9c82a3f0ddc3170a3b7f0048fda95cd8bc36e12f1b2776e9d30`  
		Last Modified: Wed, 25 Feb 2026 05:48:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:26ecebcb501bd77e320299f53c454b1fa71ded91c760f18a7a57b307a590cb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe17f8ea063134b3f66c51f892bc35b23d25ed0757fbdf82e9f165067aebfb6`

```dockerfile
```

-	Layers:
	-	`sha256:59f6b93f01b3715375164b79f6df59754d6e0902ec6a67878baa72e085964b38`  
		Last Modified: Wed, 25 Feb 2026 05:48:58 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54c874829b14d189a6001a5619763dda67a8a224b0685c5f7272e3b943c419a`  
		Last Modified: Wed, 25 Feb 2026 05:48:57 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:a39bcfa77efc7af7c937a08d332b07eb6ffee006aaafb9cd9b2d3c79f432cc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77599356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9df9d9b17e23c2dac02ed0c379d82b513e8b55c9e1fbe660cf61cad7cda9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 22:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 23:07:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:07:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 23:07:33 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 25 Feb 2026 02:39:21 GMT
ENV TINI_VERSION=0.18.0
# Wed, 25 Feb 2026 02:39:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:23 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee0a8590e769ec84c9c999b84ef7c697884603dfeac17e2f74cb19194158987`  
		Last Modified: Tue, 24 Feb 2026 23:02:46 GMT  
		Size: 3.2 MB (3171209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba25f0557aafc3759d760486d757d65a9bb3e1c108c3458785dc2ff39fc676f`  
		Last Modified: Tue, 24 Feb 2026 23:02:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8f23b843a21ce3f239a4d6af280bf2729dc51d0ac0483462479fae094340c`  
		Last Modified: Tue, 24 Feb 2026 23:07:52 GMT  
		Size: 33.1 MB (33104236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf4ff6bfa8f17cec32e84126297cd2c142213d9e37f0d2ffd9e7795450567b1`  
		Last Modified: Tue, 24 Feb 2026 23:07:50 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be13b0e8917723a0af24cbc141920b530c9a24cbe9d72925549598334842e639`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 14.4 MB (14429986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b0786c75adf02326337327216b324d581bb04e65603b8fc1dbd4a43135884`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08315f43215c0225ec306a8a7c05a553aeb6b2d2284697ad375315c7700738c0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84550c0ddc77f8b63a983e57aadb590d16013d0a2b85a5d3cbe7dc9c29ec81ca`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9df0560ccf9cc0eb9a0040a1553bbd954239feadbac3cade9b4300aa6cc969ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1e46b02eaf9f954b5ac4771b7efae352a149c78ea63c9a8cbbb716083e91da`

```dockerfile
```

-	Layers:
	-	`sha256:50f8c4edc2f854be02126e76fddc0f06a70ce49cd96b71d70cf1ce2855500131`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18427afb6fd0aaec0ae12fd27cdd134735954f8ad9f215bec007f6742693b4f0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:a3b979ff02198574027d393282b437824226abc01b560baf6cacaf1093dd346b
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
$ docker pull fluentd@sha256:98056e95ce560655b93bf9e3add0b525a759f81c075ffe847a2e1244399e2c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79241950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc77db10b97ffbddc69d46dc9a79c1d65c3d3b1b8b1425d88d6dad488bc40c3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:17:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:17:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:17:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:17:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ac34359c677603e047bdcaccffb13936db90415cd5425e19a772e106c2321`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 1.3 MB (1279325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dfdf3108059b075552a568a23ff473640e2daf0955ed48e9ddc91233660d9`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40877f1c75ec092931fd9e55b6bbe54e219d4db9a19d156104759811def3d73`  
		Last Modified: Wed, 11 Mar 2026 18:40:09 GMT  
		Size: 42.1 MB (42127122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de739fed639776f972632f3ffdfa182e9b7e5757a07c23eee68909575e9d3b`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ac0f133320bc335da9c95abc1dc4fc31b1933c84da67904793260ceada3b9`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 6.1 MB (6054470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc056f0ff48fcdc7014eea0e3415dfe68564b64192e6493aca5ddd505fbf858`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6e732aa46723bbd4ddf6d1e4f1fd258238f597500bcea984063c7789bed32`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff54ee029054b8e813346a65f20505870f97e351cd87d287bcb416058f0f2c`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:410c6d0ea78960b05d776c327a23d2d09d3585ba4560823b03770094bb53c971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e92bf16648cc1cf6d10605fc07d3a0f3bb3ad36e8c389599796f55435f4830`

```dockerfile
```

-	Layers:
	-	`sha256:bd3d8714193e4415b79965a1e0e5a20fe390d651058347f64018666ce7535075`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 2.3 MB (2281602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e41ae761368bf1302b51b81472be2f702e1b2a170c85b8905b96ea19f5440d`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:68a5254df265367ba3240ed09837659996b73d423c8aa117d3afe7dc691ae5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73093351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bb0bb4b651d7ff5b5e3b486dd363d17f4628e86a96a084ed8716ae03c888e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:35 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6321774249b9f1f6a028db4ffc2b11915c3e980c9732ee9f530f5c3569bd84`  
		Last Modified: Wed, 11 Mar 2026 18:39:27 GMT  
		Size: 1.3 MB (1262989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec27c1bcf4ae4bc343b5a1cea6d4f9c4e6aa745f051ef2c211f149803598f07`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab58b7d03dbd70019e0b0a24d6fa5f28bc2457a7d52426c4e9de48b6b0d0caa`  
		Last Modified: Wed, 11 Mar 2026 18:39:28 GMT  
		Size: 37.9 MB (37924091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3693cee0228af01605d48961da617a4156cb2151ef75ea795fd0dc33fbd7af3`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4192a4414efc21cb382168c931e6b4c348b07644fe861cd8d92c0f17ca7fc4`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 6.0 MB (5956263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e272f35dfe8731a3dfe2f513f97317a783a0d1a21c190219a11bbf45007d016`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f608bf1730643f7b338277cb73a19e443c631440ffab0bedacd404a1ccd6c7`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7de86d98e35e01f38c2a2dca1dc9e12f54cd6a9948b29e4d5f5596eb580d7e`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:875dcddf186d6a7c1ca83ad12cb280aabbff897a4f9c31aa76f7a2b36ba460af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284fbaf5dab49d5e1186cc667d05d23fd8750734fbef5643a9881221e5741e83`

```dockerfile
```

-	Layers:
	-	`sha256:2e1094a84d67cf8a9b77ae9560dbcced987c8f836ce914990a1ae6b3878cb8fe`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 2.3 MB (2284573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae864229389ba2f91d720ffff75c0a266ee621541890381cfe2a1506af2c913`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9744668bd9d7b175198981686ccd087fc0e2d54fcd4ae52a9508587f7ef56299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70957474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356c070c0ae8f1d5a86f18e6159c992e2090afc05eb80e73ecbafa4a44b3d663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:48 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0209b5ab14c5cc59c579ccd641d0afbe46c56b33a0bd99ad4e55993acfe06`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 1.2 MB (1236647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2b9c4fdd125bdaeaba20b679baaef269fbc6a6f45ae5171de3a5892623dca`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec177ea5e920d6d3a3bb9bdd4d79fea0c9d744b56c92bd8e64612a09948c6d5`  
		Last Modified: Wed, 11 Mar 2026 18:39:49 GMT  
		Size: 37.8 MB (37780192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b28d7b6b0a91bcd005637f2b7561587b89331fc0472d206b8ea8eec240756d`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423d30686507d592e38227ec924f9bd97662a25fdee7f775f3ffd1d4e7eba2d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 5.7 MB (5724488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c126699186495e24d6314913ed99194bfa184bbf7cda08cf7c85adf96d14078`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397cb9490c05559548d85714db1497d466b328d2a895de8c91c2efc5fb6667e9`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7798f2052bd0ab151a24fa244236b305efe966fa5dfe7f19f566e9fcd39665`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fbb290e1c70ac79ac172f264f7551797598697d56f34697ad4dd29dabeaf3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088bcf5bdb793831a793b6ef968d64a2f1a3c69c471b16aa1c5a98a765b89b5b`

```dockerfile
```

-	Layers:
	-	`sha256:b4bb1b78d1d4bb005109b6fac820ab004d83eec9e7a9979eef511d48e3bab666`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 2.3 MB (2283014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51aa187f24eca0e5cf6d11396dc12cec04d2728f4f16cab0c06f130f7c9db1d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4c47e798fb7a41e99b3816b96f1622ec0f8bf0b027f9ea5d3950675c965e49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0b1ee3cdff3e88ace68e382bcc71fa2110e17eb6dc41236baa40c2c882770a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bffa5cd1691dc6366ce11599d060f6c5ad180c0ad4d6810c1ac498466519d`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 1.3 MB (1261281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca28f67fe6a1ecf02ad7ce4905c032d859938153906fd15be595d38309d2e0e`  
		Last Modified: Wed, 11 Mar 2026 18:39:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b0ec96ddb91dfec10e0899ce1e8bb136293dcd72e24f2bb4f5d196126a848`  
		Last Modified: Wed, 11 Mar 2026 18:39:54 GMT  
		Size: 42.1 MB (42077901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d968e78d8934ffa4723337b3ce8e4f69ac350fe6d45486190e7eb8221faf41`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef55bac5c015d80d282bc0c7aad04233af0b956b0d37da47f686e9cbe63840d`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 6.0 MB (6043926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480f56a9c12d248c8faff32f2ee2976018eb52120ff19c05f5010301345e007`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8081c5f39e3acfcf03bb30fe7dcf87d0adf7c449b14ce4c248c420a416609cb`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221204832776264f1aa4eaef5974dcb354b7c2b77001c9f10a131d1b4939ef5b`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c1d8345d82bfa035c5fa41f17001be477894b389541645a823aa75aa72c6ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5012e26563df9e334d747dc8bebabd27f94eb87d278a38d6a292183f6b473ce`

```dockerfile
```

-	Layers:
	-	`sha256:62c7cd819c5dd97ff517bb3baaab1da5a78d7fbf161de33ec9e96a142ab39a89`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 2.3 MB (2281874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801a09bb3467020196a76bc15ad49a4568bd3079f387e4a563934d3f562014e4`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:a34f4faef125d2c1c0b7bd866ca0e3132e10cbc6cd2656b7556a2f267618a1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd2a7233616b14025152fae14adbf8d1fc10e410271edbcbf38eeea4d8f413`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:02 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:02 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:02 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88f57d04c7cfe5bb1217bad3e3ff16c30aea89aaade4ec661e53853315a02b`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 1.3 MB (1287310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447bad7b66208f8e935f58d734a53f366f3d6017c5a21abe67c4dd2540f77efb`  
		Last Modified: Wed, 11 Mar 2026 18:31:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dd3c17eee9b3bf39cca9d43f8ff495a7c75199811b65bda5f566afbe968fe`  
		Last Modified: Wed, 11 Mar 2026 18:31:56 GMT  
		Size: 37.7 MB (37661725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00ce345593bb8166503f9a71eeb0eec086b76f9b8ee5d85378d6ce7384165d`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d889071b4c31131058eb1717f21630ae829bf20236346853191378472378`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 6.0 MB (6025573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd2386539996dd7ecbb76d8338b4e6ba89be42afd48f6e7f4ee160816220458`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e088c0c3706d7a1de6a2a99084988cb91ba507a308c257bb4e2d242023049df`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13c7afe2833b7e6653f6d520c277980f2e7a7621d992f45dc898511516b52c`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2f589f391f45d80df48ea7b5a8d3ba4a2f836763858f99aa95b3ab3e934cf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f93cc26b17337c0c4f8bdd44ea80516d4fb2bb69783f1696fbf270c18371647`

```dockerfile
```

-	Layers:
	-	`sha256:ba093f17127866de97e95fda615ecbac913309fe75b394d315796d3e2ca85a12`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 2.3 MB (2278790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b5868101a72b0da8c025457d3c4d4e1e55a5296194e5614c043c2c4593900f`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de8d3ad6ce1849bf7b5f28006b9212783ef94e4561909d461485a8fc1d8257ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81019590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52803c668efdfed3a0b2398ea8ef2d6dfe238fc97d6e040701d543478b16aa51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:45:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:45:49 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:22:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:22:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:22:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:22:18 GMT
USER fluent
# Wed, 11 Mar 2026 19:22:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:22:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bba5358e3f378909e4c0a9cb9af69228f3108fd67a587461fccd3158cb37a6`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 1.3 MB (1309516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bde25b75aac9ba75f7885fbf7286727e870ee78b380c72bc612e409b3f55ce`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928678f951f229519de045ee3851c120dd40d5a36fe1846396e5695cfd5f76c`  
		Last Modified: Wed, 11 Mar 2026 18:46:07 GMT  
		Size: 39.5 MB (39531725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b362d31236d551dffe973f43a7c056cf3d2c5be3d482402a299b46c47d7bbde`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca75c809c185b8b9b3af8851c647e673b0c586e1a1b9afc4085e682cdda7a10`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 6.6 MB (6575733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf00919f179c5e952b990fdaee3167ae0855465c1648e9d6ce0dbb6254aa0c4`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b58f73d83f66b53787162bd9f95f7898ac610e24cda3db51a3bd3222d7806`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc55a1d404e92beb7cc18af679e3b12fd3567c6e4e86adda49137e2f24657aa7`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e134ec73a0dfba5d8cb13f30e4967ab90a3cbccb35389ee43f15b5e8b9d994a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777a754e5615e3f977cb9a52c9c13ac48bd2fde7739a3cec265f9fcd8900344`

```dockerfile
```

-	Layers:
	-	`sha256:895467fd95e7f9047a1b753596a06673f51c2442449f6a0ea05847c089380b8c`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 2.3 MB (2285137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebe8cc4e199aa617ed31aabf514d168691d23c17158c4343019e5025a4f5c47`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:15272769816a339589731725f28014f3cf73e0416f3f0d3afd2ac0dbfb6a95b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3375b66a23ddd0134dfa3c5f5af79b3e2c54f6f5cbcf892481165aa944ff24c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:44 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2330c467e1931fe73b76bbfce21eb00bbeb1b3408d0f700032ddcb64bb358b`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 1.3 MB (1294488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342513ff2afeeee15c2a6131bc1f9b6bda0e30048d575aa73c13abe3642f4ac4`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096e51e12f56f8972511878c2bdd53785b95467ddc2431a3ed08203e984dfb2`  
		Last Modified: Wed, 11 Mar 2026 18:33:47 GMT  
		Size: 39.2 MB (39205804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c44d6373d7f22f1af2eea10934cea9eef1965e287d8d54f607bda53e16f41`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059721229294da070222585983b257cd6ca81f01a46688fb93366f12f193c09`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 6.4 MB (6429931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff45129a091c48baccc63e67d8f470f5b5c610992ac341d2ca285e35ef3965`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf75ab18f67fb4f9382c309c081e6dbc0fcc15822f4b2fbc758b6db88843aec`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9056a71b599985194f6a6956b6a3879d3c1dd3eb967f2daefff034e1c312f8`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:71504d474cab676e050e9baa575e5eb76234b6a52da2e426ba13b5bd4a2d05ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a78d1b92735b8fbf7a02be684de548f50814027e99dce875d8f8a819f2cc9`

```dockerfile
```

-	Layers:
	-	`sha256:f02789c7eaf625e4c19a111f65e5d6fbe7d3cc7f4fdb8f430a2480298891066d`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 2.3 MB (2283047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a433fca29ae7cbd3a34d6df5ae84cc11f5dbda5e3bb534023f73842d62a6bb19`  
		Last Modified: Wed, 11 Mar 2026 19:15:57 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:a3b979ff02198574027d393282b437824226abc01b560baf6cacaf1093dd346b
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
$ docker pull fluentd@sha256:98056e95ce560655b93bf9e3add0b525a759f81c075ffe847a2e1244399e2c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79241950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc77db10b97ffbddc69d46dc9a79c1d65c3d3b1b8b1425d88d6dad488bc40c3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:17:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:17:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:17:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:17:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ac34359c677603e047bdcaccffb13936db90415cd5425e19a772e106c2321`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 1.3 MB (1279325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dfdf3108059b075552a568a23ff473640e2daf0955ed48e9ddc91233660d9`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40877f1c75ec092931fd9e55b6bbe54e219d4db9a19d156104759811def3d73`  
		Last Modified: Wed, 11 Mar 2026 18:40:09 GMT  
		Size: 42.1 MB (42127122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de739fed639776f972632f3ffdfa182e9b7e5757a07c23eee68909575e9d3b`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ac0f133320bc335da9c95abc1dc4fc31b1933c84da67904793260ceada3b9`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 6.1 MB (6054470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc056f0ff48fcdc7014eea0e3415dfe68564b64192e6493aca5ddd505fbf858`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6e732aa46723bbd4ddf6d1e4f1fd258238f597500bcea984063c7789bed32`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff54ee029054b8e813346a65f20505870f97e351cd87d287bcb416058f0f2c`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:410c6d0ea78960b05d776c327a23d2d09d3585ba4560823b03770094bb53c971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e92bf16648cc1cf6d10605fc07d3a0f3bb3ad36e8c389599796f55435f4830`

```dockerfile
```

-	Layers:
	-	`sha256:bd3d8714193e4415b79965a1e0e5a20fe390d651058347f64018666ce7535075`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 2.3 MB (2281602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e41ae761368bf1302b51b81472be2f702e1b2a170c85b8905b96ea19f5440d`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:68a5254df265367ba3240ed09837659996b73d423c8aa117d3afe7dc691ae5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73093351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bb0bb4b651d7ff5b5e3b486dd363d17f4628e86a96a084ed8716ae03c888e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:35 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6321774249b9f1f6a028db4ffc2b11915c3e980c9732ee9f530f5c3569bd84`  
		Last Modified: Wed, 11 Mar 2026 18:39:27 GMT  
		Size: 1.3 MB (1262989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec27c1bcf4ae4bc343b5a1cea6d4f9c4e6aa745f051ef2c211f149803598f07`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab58b7d03dbd70019e0b0a24d6fa5f28bc2457a7d52426c4e9de48b6b0d0caa`  
		Last Modified: Wed, 11 Mar 2026 18:39:28 GMT  
		Size: 37.9 MB (37924091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3693cee0228af01605d48961da617a4156cb2151ef75ea795fd0dc33fbd7af3`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4192a4414efc21cb382168c931e6b4c348b07644fe861cd8d92c0f17ca7fc4`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 6.0 MB (5956263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e272f35dfe8731a3dfe2f513f97317a783a0d1a21c190219a11bbf45007d016`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f608bf1730643f7b338277cb73a19e443c631440ffab0bedacd404a1ccd6c7`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7de86d98e35e01f38c2a2dca1dc9e12f54cd6a9948b29e4d5f5596eb580d7e`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:875dcddf186d6a7c1ca83ad12cb280aabbff897a4f9c31aa76f7a2b36ba460af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284fbaf5dab49d5e1186cc667d05d23fd8750734fbef5643a9881221e5741e83`

```dockerfile
```

-	Layers:
	-	`sha256:2e1094a84d67cf8a9b77ae9560dbcced987c8f836ce914990a1ae6b3878cb8fe`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 2.3 MB (2284573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae864229389ba2f91d720ffff75c0a266ee621541890381cfe2a1506af2c913`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9744668bd9d7b175198981686ccd087fc0e2d54fcd4ae52a9508587f7ef56299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70957474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356c070c0ae8f1d5a86f18e6159c992e2090afc05eb80e73ecbafa4a44b3d663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:48 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0209b5ab14c5cc59c579ccd641d0afbe46c56b33a0bd99ad4e55993acfe06`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 1.2 MB (1236647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2b9c4fdd125bdaeaba20b679baaef269fbc6a6f45ae5171de3a5892623dca`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec177ea5e920d6d3a3bb9bdd4d79fea0c9d744b56c92bd8e64612a09948c6d5`  
		Last Modified: Wed, 11 Mar 2026 18:39:49 GMT  
		Size: 37.8 MB (37780192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b28d7b6b0a91bcd005637f2b7561587b89331fc0472d206b8ea8eec240756d`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423d30686507d592e38227ec924f9bd97662a25fdee7f775f3ffd1d4e7eba2d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 5.7 MB (5724488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c126699186495e24d6314913ed99194bfa184bbf7cda08cf7c85adf96d14078`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397cb9490c05559548d85714db1497d466b328d2a895de8c91c2efc5fb6667e9`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7798f2052bd0ab151a24fa244236b305efe966fa5dfe7f19f566e9fcd39665`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fbb290e1c70ac79ac172f264f7551797598697d56f34697ad4dd29dabeaf3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088bcf5bdb793831a793b6ef968d64a2f1a3c69c471b16aa1c5a98a765b89b5b`

```dockerfile
```

-	Layers:
	-	`sha256:b4bb1b78d1d4bb005109b6fac820ab004d83eec9e7a9979eef511d48e3bab666`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 2.3 MB (2283014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51aa187f24eca0e5cf6d11396dc12cec04d2728f4f16cab0c06f130f7c9db1d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4c47e798fb7a41e99b3816b96f1622ec0f8bf0b027f9ea5d3950675c965e49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0b1ee3cdff3e88ace68e382bcc71fa2110e17eb6dc41236baa40c2c882770a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bffa5cd1691dc6366ce11599d060f6c5ad180c0ad4d6810c1ac498466519d`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 1.3 MB (1261281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca28f67fe6a1ecf02ad7ce4905c032d859938153906fd15be595d38309d2e0e`  
		Last Modified: Wed, 11 Mar 2026 18:39:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b0ec96ddb91dfec10e0899ce1e8bb136293dcd72e24f2bb4f5d196126a848`  
		Last Modified: Wed, 11 Mar 2026 18:39:54 GMT  
		Size: 42.1 MB (42077901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d968e78d8934ffa4723337b3ce8e4f69ac350fe6d45486190e7eb8221faf41`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef55bac5c015d80d282bc0c7aad04233af0b956b0d37da47f686e9cbe63840d`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 6.0 MB (6043926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480f56a9c12d248c8faff32f2ee2976018eb52120ff19c05f5010301345e007`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8081c5f39e3acfcf03bb30fe7dcf87d0adf7c449b14ce4c248c420a416609cb`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221204832776264f1aa4eaef5974dcb354b7c2b77001c9f10a131d1b4939ef5b`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c1d8345d82bfa035c5fa41f17001be477894b389541645a823aa75aa72c6ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5012e26563df9e334d747dc8bebabd27f94eb87d278a38d6a292183f6b473ce`

```dockerfile
```

-	Layers:
	-	`sha256:62c7cd819c5dd97ff517bb3baaab1da5a78d7fbf161de33ec9e96a142ab39a89`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 2.3 MB (2281874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801a09bb3467020196a76bc15ad49a4568bd3079f387e4a563934d3f562014e4`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:a34f4faef125d2c1c0b7bd866ca0e3132e10cbc6cd2656b7556a2f267618a1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd2a7233616b14025152fae14adbf8d1fc10e410271edbcbf38eeea4d8f413`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:02 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:02 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:02 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88f57d04c7cfe5bb1217bad3e3ff16c30aea89aaade4ec661e53853315a02b`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 1.3 MB (1287310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447bad7b66208f8e935f58d734a53f366f3d6017c5a21abe67c4dd2540f77efb`  
		Last Modified: Wed, 11 Mar 2026 18:31:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dd3c17eee9b3bf39cca9d43f8ff495a7c75199811b65bda5f566afbe968fe`  
		Last Modified: Wed, 11 Mar 2026 18:31:56 GMT  
		Size: 37.7 MB (37661725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00ce345593bb8166503f9a71eeb0eec086b76f9b8ee5d85378d6ce7384165d`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d889071b4c31131058eb1717f21630ae829bf20236346853191378472378`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 6.0 MB (6025573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd2386539996dd7ecbb76d8338b4e6ba89be42afd48f6e7f4ee160816220458`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e088c0c3706d7a1de6a2a99084988cb91ba507a308c257bb4e2d242023049df`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13c7afe2833b7e6653f6d520c277980f2e7a7621d992f45dc898511516b52c`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2f589f391f45d80df48ea7b5a8d3ba4a2f836763858f99aa95b3ab3e934cf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f93cc26b17337c0c4f8bdd44ea80516d4fb2bb69783f1696fbf270c18371647`

```dockerfile
```

-	Layers:
	-	`sha256:ba093f17127866de97e95fda615ecbac913309fe75b394d315796d3e2ca85a12`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 2.3 MB (2278790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b5868101a72b0da8c025457d3c4d4e1e55a5296194e5614c043c2c4593900f`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de8d3ad6ce1849bf7b5f28006b9212783ef94e4561909d461485a8fc1d8257ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81019590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52803c668efdfed3a0b2398ea8ef2d6dfe238fc97d6e040701d543478b16aa51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:45:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:45:49 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:22:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:22:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:22:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:22:18 GMT
USER fluent
# Wed, 11 Mar 2026 19:22:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:22:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bba5358e3f378909e4c0a9cb9af69228f3108fd67a587461fccd3158cb37a6`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 1.3 MB (1309516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bde25b75aac9ba75f7885fbf7286727e870ee78b380c72bc612e409b3f55ce`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928678f951f229519de045ee3851c120dd40d5a36fe1846396e5695cfd5f76c`  
		Last Modified: Wed, 11 Mar 2026 18:46:07 GMT  
		Size: 39.5 MB (39531725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b362d31236d551dffe973f43a7c056cf3d2c5be3d482402a299b46c47d7bbde`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca75c809c185b8b9b3af8851c647e673b0c586e1a1b9afc4085e682cdda7a10`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 6.6 MB (6575733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf00919f179c5e952b990fdaee3167ae0855465c1648e9d6ce0dbb6254aa0c4`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b58f73d83f66b53787162bd9f95f7898ac610e24cda3db51a3bd3222d7806`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc55a1d404e92beb7cc18af679e3b12fd3567c6e4e86adda49137e2f24657aa7`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e134ec73a0dfba5d8cb13f30e4967ab90a3cbccb35389ee43f15b5e8b9d994a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777a754e5615e3f977cb9a52c9c13ac48bd2fde7739a3cec265f9fcd8900344`

```dockerfile
```

-	Layers:
	-	`sha256:895467fd95e7f9047a1b753596a06673f51c2442449f6a0ea05847c089380b8c`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 2.3 MB (2285137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebe8cc4e199aa617ed31aabf514d168691d23c17158c4343019e5025a4f5c47`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:15272769816a339589731725f28014f3cf73e0416f3f0d3afd2ac0dbfb6a95b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3375b66a23ddd0134dfa3c5f5af79b3e2c54f6f5cbcf892481165aa944ff24c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:44 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2330c467e1931fe73b76bbfce21eb00bbeb1b3408d0f700032ddcb64bb358b`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 1.3 MB (1294488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342513ff2afeeee15c2a6131bc1f9b6bda0e30048d575aa73c13abe3642f4ac4`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096e51e12f56f8972511878c2bdd53785b95467ddc2431a3ed08203e984dfb2`  
		Last Modified: Wed, 11 Mar 2026 18:33:47 GMT  
		Size: 39.2 MB (39205804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c44d6373d7f22f1af2eea10934cea9eef1965e287d8d54f607bda53e16f41`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059721229294da070222585983b257cd6ca81f01a46688fb93366f12f193c09`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 6.4 MB (6429931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff45129a091c48baccc63e67d8f470f5b5c610992ac341d2ca285e35ef3965`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf75ab18f67fb4f9382c309c081e6dbc0fcc15822f4b2fbc758b6db88843aec`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9056a71b599985194f6a6956b6a3879d3c1dd3eb967f2daefff034e1c312f8`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:71504d474cab676e050e9baa575e5eb76234b6a52da2e426ba13b5bd4a2d05ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a78d1b92735b8fbf7a02be684de548f50814027e99dce875d8f8a819f2cc9`

```dockerfile
```

-	Layers:
	-	`sha256:f02789c7eaf625e4c19a111f65e5d6fbe7d3cc7f4fdb8f430a2480298891066d`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 2.3 MB (2283047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a433fca29ae7cbd3a34d6df5ae84cc11f5dbda5e3bb534023f73842d62a6bb19`  
		Last Modified: Wed, 11 Mar 2026 19:15:57 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:a3b979ff02198574027d393282b437824226abc01b560baf6cacaf1093dd346b
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
$ docker pull fluentd@sha256:98056e95ce560655b93bf9e3add0b525a759f81c075ffe847a2e1244399e2c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79241950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc77db10b97ffbddc69d46dc9a79c1d65c3d3b1b8b1425d88d6dad488bc40c3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:17:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:17:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:17:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:17:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ac34359c677603e047bdcaccffb13936db90415cd5425e19a772e106c2321`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 1.3 MB (1279325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dfdf3108059b075552a568a23ff473640e2daf0955ed48e9ddc91233660d9`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40877f1c75ec092931fd9e55b6bbe54e219d4db9a19d156104759811def3d73`  
		Last Modified: Wed, 11 Mar 2026 18:40:09 GMT  
		Size: 42.1 MB (42127122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de739fed639776f972632f3ffdfa182e9b7e5757a07c23eee68909575e9d3b`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ac0f133320bc335da9c95abc1dc4fc31b1933c84da67904793260ceada3b9`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 6.1 MB (6054470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc056f0ff48fcdc7014eea0e3415dfe68564b64192e6493aca5ddd505fbf858`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6e732aa46723bbd4ddf6d1e4f1fd258238f597500bcea984063c7789bed32`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff54ee029054b8e813346a65f20505870f97e351cd87d287bcb416058f0f2c`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:410c6d0ea78960b05d776c327a23d2d09d3585ba4560823b03770094bb53c971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e92bf16648cc1cf6d10605fc07d3a0f3bb3ad36e8c389599796f55435f4830`

```dockerfile
```

-	Layers:
	-	`sha256:bd3d8714193e4415b79965a1e0e5a20fe390d651058347f64018666ce7535075`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 2.3 MB (2281602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e41ae761368bf1302b51b81472be2f702e1b2a170c85b8905b96ea19f5440d`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:68a5254df265367ba3240ed09837659996b73d423c8aa117d3afe7dc691ae5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73093351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bb0bb4b651d7ff5b5e3b486dd363d17f4628e86a96a084ed8716ae03c888e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:35 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6321774249b9f1f6a028db4ffc2b11915c3e980c9732ee9f530f5c3569bd84`  
		Last Modified: Wed, 11 Mar 2026 18:39:27 GMT  
		Size: 1.3 MB (1262989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec27c1bcf4ae4bc343b5a1cea6d4f9c4e6aa745f051ef2c211f149803598f07`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab58b7d03dbd70019e0b0a24d6fa5f28bc2457a7d52426c4e9de48b6b0d0caa`  
		Last Modified: Wed, 11 Mar 2026 18:39:28 GMT  
		Size: 37.9 MB (37924091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3693cee0228af01605d48961da617a4156cb2151ef75ea795fd0dc33fbd7af3`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4192a4414efc21cb382168c931e6b4c348b07644fe861cd8d92c0f17ca7fc4`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 6.0 MB (5956263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e272f35dfe8731a3dfe2f513f97317a783a0d1a21c190219a11bbf45007d016`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f608bf1730643f7b338277cb73a19e443c631440ffab0bedacd404a1ccd6c7`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7de86d98e35e01f38c2a2dca1dc9e12f54cd6a9948b29e4d5f5596eb580d7e`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:875dcddf186d6a7c1ca83ad12cb280aabbff897a4f9c31aa76f7a2b36ba460af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284fbaf5dab49d5e1186cc667d05d23fd8750734fbef5643a9881221e5741e83`

```dockerfile
```

-	Layers:
	-	`sha256:2e1094a84d67cf8a9b77ae9560dbcced987c8f836ce914990a1ae6b3878cb8fe`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 2.3 MB (2284573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae864229389ba2f91d720ffff75c0a266ee621541890381cfe2a1506af2c913`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9744668bd9d7b175198981686ccd087fc0e2d54fcd4ae52a9508587f7ef56299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70957474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356c070c0ae8f1d5a86f18e6159c992e2090afc05eb80e73ecbafa4a44b3d663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:48 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0209b5ab14c5cc59c579ccd641d0afbe46c56b33a0bd99ad4e55993acfe06`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 1.2 MB (1236647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2b9c4fdd125bdaeaba20b679baaef269fbc6a6f45ae5171de3a5892623dca`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec177ea5e920d6d3a3bb9bdd4d79fea0c9d744b56c92bd8e64612a09948c6d5`  
		Last Modified: Wed, 11 Mar 2026 18:39:49 GMT  
		Size: 37.8 MB (37780192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b28d7b6b0a91bcd005637f2b7561587b89331fc0472d206b8ea8eec240756d`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423d30686507d592e38227ec924f9bd97662a25fdee7f775f3ffd1d4e7eba2d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 5.7 MB (5724488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c126699186495e24d6314913ed99194bfa184bbf7cda08cf7c85adf96d14078`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397cb9490c05559548d85714db1497d466b328d2a895de8c91c2efc5fb6667e9`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7798f2052bd0ab151a24fa244236b305efe966fa5dfe7f19f566e9fcd39665`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fbb290e1c70ac79ac172f264f7551797598697d56f34697ad4dd29dabeaf3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088bcf5bdb793831a793b6ef968d64a2f1a3c69c471b16aa1c5a98a765b89b5b`

```dockerfile
```

-	Layers:
	-	`sha256:b4bb1b78d1d4bb005109b6fac820ab004d83eec9e7a9979eef511d48e3bab666`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 2.3 MB (2283014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51aa187f24eca0e5cf6d11396dc12cec04d2728f4f16cab0c06f130f7c9db1d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4c47e798fb7a41e99b3816b96f1622ec0f8bf0b027f9ea5d3950675c965e49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0b1ee3cdff3e88ace68e382bcc71fa2110e17eb6dc41236baa40c2c882770a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bffa5cd1691dc6366ce11599d060f6c5ad180c0ad4d6810c1ac498466519d`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 1.3 MB (1261281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca28f67fe6a1ecf02ad7ce4905c032d859938153906fd15be595d38309d2e0e`  
		Last Modified: Wed, 11 Mar 2026 18:39:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b0ec96ddb91dfec10e0899ce1e8bb136293dcd72e24f2bb4f5d196126a848`  
		Last Modified: Wed, 11 Mar 2026 18:39:54 GMT  
		Size: 42.1 MB (42077901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d968e78d8934ffa4723337b3ce8e4f69ac350fe6d45486190e7eb8221faf41`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef55bac5c015d80d282bc0c7aad04233af0b956b0d37da47f686e9cbe63840d`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 6.0 MB (6043926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480f56a9c12d248c8faff32f2ee2976018eb52120ff19c05f5010301345e007`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8081c5f39e3acfcf03bb30fe7dcf87d0adf7c449b14ce4c248c420a416609cb`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221204832776264f1aa4eaef5974dcb354b7c2b77001c9f10a131d1b4939ef5b`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c1d8345d82bfa035c5fa41f17001be477894b389541645a823aa75aa72c6ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5012e26563df9e334d747dc8bebabd27f94eb87d278a38d6a292183f6b473ce`

```dockerfile
```

-	Layers:
	-	`sha256:62c7cd819c5dd97ff517bb3baaab1da5a78d7fbf161de33ec9e96a142ab39a89`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 2.3 MB (2281874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801a09bb3467020196a76bc15ad49a4568bd3079f387e4a563934d3f562014e4`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:a34f4faef125d2c1c0b7bd866ca0e3132e10cbc6cd2656b7556a2f267618a1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd2a7233616b14025152fae14adbf8d1fc10e410271edbcbf38eeea4d8f413`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:02 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:02 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:02 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88f57d04c7cfe5bb1217bad3e3ff16c30aea89aaade4ec661e53853315a02b`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 1.3 MB (1287310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447bad7b66208f8e935f58d734a53f366f3d6017c5a21abe67c4dd2540f77efb`  
		Last Modified: Wed, 11 Mar 2026 18:31:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dd3c17eee9b3bf39cca9d43f8ff495a7c75199811b65bda5f566afbe968fe`  
		Last Modified: Wed, 11 Mar 2026 18:31:56 GMT  
		Size: 37.7 MB (37661725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00ce345593bb8166503f9a71eeb0eec086b76f9b8ee5d85378d6ce7384165d`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d889071b4c31131058eb1717f21630ae829bf20236346853191378472378`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 6.0 MB (6025573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd2386539996dd7ecbb76d8338b4e6ba89be42afd48f6e7f4ee160816220458`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e088c0c3706d7a1de6a2a99084988cb91ba507a308c257bb4e2d242023049df`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13c7afe2833b7e6653f6d520c277980f2e7a7621d992f45dc898511516b52c`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2f589f391f45d80df48ea7b5a8d3ba4a2f836763858f99aa95b3ab3e934cf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f93cc26b17337c0c4f8bdd44ea80516d4fb2bb69783f1696fbf270c18371647`

```dockerfile
```

-	Layers:
	-	`sha256:ba093f17127866de97e95fda615ecbac913309fe75b394d315796d3e2ca85a12`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 2.3 MB (2278790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b5868101a72b0da8c025457d3c4d4e1e55a5296194e5614c043c2c4593900f`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de8d3ad6ce1849bf7b5f28006b9212783ef94e4561909d461485a8fc1d8257ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81019590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52803c668efdfed3a0b2398ea8ef2d6dfe238fc97d6e040701d543478b16aa51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:45:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:45:49 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:22:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:22:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:22:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:22:18 GMT
USER fluent
# Wed, 11 Mar 2026 19:22:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:22:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bba5358e3f378909e4c0a9cb9af69228f3108fd67a587461fccd3158cb37a6`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 1.3 MB (1309516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bde25b75aac9ba75f7885fbf7286727e870ee78b380c72bc612e409b3f55ce`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928678f951f229519de045ee3851c120dd40d5a36fe1846396e5695cfd5f76c`  
		Last Modified: Wed, 11 Mar 2026 18:46:07 GMT  
		Size: 39.5 MB (39531725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b362d31236d551dffe973f43a7c056cf3d2c5be3d482402a299b46c47d7bbde`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca75c809c185b8b9b3af8851c647e673b0c586e1a1b9afc4085e682cdda7a10`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 6.6 MB (6575733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf00919f179c5e952b990fdaee3167ae0855465c1648e9d6ce0dbb6254aa0c4`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b58f73d83f66b53787162bd9f95f7898ac610e24cda3db51a3bd3222d7806`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc55a1d404e92beb7cc18af679e3b12fd3567c6e4e86adda49137e2f24657aa7`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e134ec73a0dfba5d8cb13f30e4967ab90a3cbccb35389ee43f15b5e8b9d994a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777a754e5615e3f977cb9a52c9c13ac48bd2fde7739a3cec265f9fcd8900344`

```dockerfile
```

-	Layers:
	-	`sha256:895467fd95e7f9047a1b753596a06673f51c2442449f6a0ea05847c089380b8c`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 2.3 MB (2285137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebe8cc4e199aa617ed31aabf514d168691d23c17158c4343019e5025a4f5c47`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:15272769816a339589731725f28014f3cf73e0416f3f0d3afd2ac0dbfb6a95b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3375b66a23ddd0134dfa3c5f5af79b3e2c54f6f5cbcf892481165aa944ff24c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:44 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2330c467e1931fe73b76bbfce21eb00bbeb1b3408d0f700032ddcb64bb358b`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 1.3 MB (1294488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342513ff2afeeee15c2a6131bc1f9b6bda0e30048d575aa73c13abe3642f4ac4`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096e51e12f56f8972511878c2bdd53785b95467ddc2431a3ed08203e984dfb2`  
		Last Modified: Wed, 11 Mar 2026 18:33:47 GMT  
		Size: 39.2 MB (39205804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c44d6373d7f22f1af2eea10934cea9eef1965e287d8d54f607bda53e16f41`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059721229294da070222585983b257cd6ca81f01a46688fb93366f12f193c09`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 6.4 MB (6429931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff45129a091c48baccc63e67d8f470f5b5c610992ac341d2ca285e35ef3965`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf75ab18f67fb4f9382c309c081e6dbc0fcc15822f4b2fbc758b6db88843aec`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9056a71b599985194f6a6956b6a3879d3c1dd3eb967f2daefff034e1c312f8`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:71504d474cab676e050e9baa575e5eb76234b6a52da2e426ba13b5bd4a2d05ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a78d1b92735b8fbf7a02be684de548f50814027e99dce875d8f8a819f2cc9`

```dockerfile
```

-	Layers:
	-	`sha256:f02789c7eaf625e4c19a111f65e5d6fbe7d3cc7f4fdb8f430a2480298891066d`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 2.3 MB (2283047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a433fca29ae7cbd3a34d6df5ae84cc11f5dbda5e3bb534023f73842d62a6bb19`  
		Last Modified: Wed, 11 Mar 2026 19:15:57 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:a3b979ff02198574027d393282b437824226abc01b560baf6cacaf1093dd346b
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
$ docker pull fluentd@sha256:98056e95ce560655b93bf9e3add0b525a759f81c075ffe847a2e1244399e2c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79241950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc77db10b97ffbddc69d46dc9a79c1d65c3d3b1b8b1425d88d6dad488bc40c3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:59 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:59 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:17:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:17:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:17:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:17:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:17:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:17:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ac34359c677603e047bdcaccffb13936db90415cd5425e19a772e106c2321`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 1.3 MB (1279325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dfdf3108059b075552a568a23ff473640e2daf0955ed48e9ddc91233660d9`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40877f1c75ec092931fd9e55b6bbe54e219d4db9a19d156104759811def3d73`  
		Last Modified: Wed, 11 Mar 2026 18:40:09 GMT  
		Size: 42.1 MB (42127122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de739fed639776f972632f3ffdfa182e9b7e5757a07c23eee68909575e9d3b`  
		Last Modified: Wed, 11 Mar 2026 18:40:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ac0f133320bc335da9c95abc1dc4fc31b1933c84da67904793260ceada3b9`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 6.1 MB (6054470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc056f0ff48fcdc7014eea0e3415dfe68564b64192e6493aca5ddd505fbf858`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6e732aa46723bbd4ddf6d1e4f1fd258238f597500bcea984063c7789bed32`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff54ee029054b8e813346a65f20505870f97e351cd87d287bcb416058f0f2c`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:410c6d0ea78960b05d776c327a23d2d09d3585ba4560823b03770094bb53c971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e92bf16648cc1cf6d10605fc07d3a0f3bb3ad36e8c389599796f55435f4830`

```dockerfile
```

-	Layers:
	-	`sha256:bd3d8714193e4415b79965a1e0e5a20fe390d651058347f64018666ce7535075`  
		Last Modified: Wed, 11 Mar 2026 19:17:35 GMT  
		Size: 2.3 MB (2281602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e41ae761368bf1302b51b81472be2f702e1b2a170c85b8905b96ea19f5440d`  
		Last Modified: Wed, 11 Mar 2026 19:17:34 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:68a5254df265367ba3240ed09837659996b73d423c8aa117d3afe7dc691ae5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73093351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bb0bb4b651d7ff5b5e3b486dd363d17f4628e86a96a084ed8716ae03c888e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:18 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:18 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:35 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6321774249b9f1f6a028db4ffc2b11915c3e980c9732ee9f530f5c3569bd84`  
		Last Modified: Wed, 11 Mar 2026 18:39:27 GMT  
		Size: 1.3 MB (1262989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec27c1bcf4ae4bc343b5a1cea6d4f9c4e6aa745f051ef2c211f149803598f07`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab58b7d03dbd70019e0b0a24d6fa5f28bc2457a7d52426c4e9de48b6b0d0caa`  
		Last Modified: Wed, 11 Mar 2026 18:39:28 GMT  
		Size: 37.9 MB (37924091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3693cee0228af01605d48961da617a4156cb2151ef75ea795fd0dc33fbd7af3`  
		Last Modified: Wed, 11 Mar 2026 18:39:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4192a4414efc21cb382168c931e6b4c348b07644fe861cd8d92c0f17ca7fc4`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 6.0 MB (5956263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e272f35dfe8731a3dfe2f513f97317a783a0d1a21c190219a11bbf45007d016`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f608bf1730643f7b338277cb73a19e443c631440ffab0bedacd404a1ccd6c7`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7de86d98e35e01f38c2a2dca1dc9e12f54cd6a9948b29e4d5f5596eb580d7e`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:875dcddf186d6a7c1ca83ad12cb280aabbff897a4f9c31aa76f7a2b36ba460af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284fbaf5dab49d5e1186cc667d05d23fd8750734fbef5643a9881221e5741e83`

```dockerfile
```

-	Layers:
	-	`sha256:2e1094a84d67cf8a9b77ae9560dbcced987c8f836ce914990a1ae6b3878cb8fe`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 2.3 MB (2284573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae864229389ba2f91d720ffff75c0a266ee621541890381cfe2a1506af2c913`  
		Last Modified: Wed, 11 Mar 2026 19:15:43 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9744668bd9d7b175198981686ccd087fc0e2d54fcd4ae52a9508587f7ef56299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70957474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356c070c0ae8f1d5a86f18e6159c992e2090afc05eb80e73ecbafa4a44b3d663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:36:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:40 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:48 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0209b5ab14c5cc59c579ccd641d0afbe46c56b33a0bd99ad4e55993acfe06`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 1.2 MB (1236647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2b9c4fdd125bdaeaba20b679baaef269fbc6a6f45ae5171de3a5892623dca`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec177ea5e920d6d3a3bb9bdd4d79fea0c9d744b56c92bd8e64612a09948c6d5`  
		Last Modified: Wed, 11 Mar 2026 18:39:49 GMT  
		Size: 37.8 MB (37780192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b28d7b6b0a91bcd005637f2b7561587b89331fc0472d206b8ea8eec240756d`  
		Last Modified: Wed, 11 Mar 2026 18:39:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423d30686507d592e38227ec924f9bd97662a25fdee7f775f3ffd1d4e7eba2d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 5.7 MB (5724488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c126699186495e24d6314913ed99194bfa184bbf7cda08cf7c85adf96d14078`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397cb9490c05559548d85714db1497d466b328d2a895de8c91c2efc5fb6667e9`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7798f2052bd0ab151a24fa244236b305efe966fa5dfe7f19f566e9fcd39665`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fbb290e1c70ac79ac172f264f7551797598697d56f34697ad4dd29dabeaf3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088bcf5bdb793831a793b6ef968d64a2f1a3c69c471b16aa1c5a98a765b89b5b`

```dockerfile
```

-	Layers:
	-	`sha256:b4bb1b78d1d4bb005109b6fac820ab004d83eec9e7a9979eef511d48e3bab666`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 2.3 MB (2283014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51aa187f24eca0e5cf6d11396dc12cec04d2728f4f16cab0c06f130f7c9db1d`  
		Last Modified: Wed, 11 Mar 2026 19:18:56 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4c47e798fb7a41e99b3816b96f1622ec0f8bf0b027f9ea5d3950675c965e49d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79525606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0b1ee3cdff3e88ace68e382bcc71fa2110e17eb6dc41236baa40c2c882770a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:37:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:39:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:39:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:39:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:39:44 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:18:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:18:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:18:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:18:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:18:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:18:27 GMT
USER fluent
# Wed, 11 Mar 2026 19:18:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:18:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bffa5cd1691dc6366ce11599d060f6c5ad180c0ad4d6810c1ac498466519d`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 1.3 MB (1261281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca28f67fe6a1ecf02ad7ce4905c032d859938153906fd15be595d38309d2e0e`  
		Last Modified: Wed, 11 Mar 2026 18:39:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b0ec96ddb91dfec10e0899ce1e8bb136293dcd72e24f2bb4f5d196126a848`  
		Last Modified: Wed, 11 Mar 2026 18:39:54 GMT  
		Size: 42.1 MB (42077901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d968e78d8934ffa4723337b3ce8e4f69ac350fe6d45486190e7eb8221faf41`  
		Last Modified: Wed, 11 Mar 2026 18:39:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef55bac5c015d80d282bc0c7aad04233af0b956b0d37da47f686e9cbe63840d`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 6.0 MB (6043926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480f56a9c12d248c8faff32f2ee2976018eb52120ff19c05f5010301345e007`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8081c5f39e3acfcf03bb30fe7dcf87d0adf7c449b14ce4c248c420a416609cb`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221204832776264f1aa4eaef5974dcb354b7c2b77001c9f10a131d1b4939ef5b`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c1d8345d82bfa035c5fa41f17001be477894b389541645a823aa75aa72c6ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5012e26563df9e334d747dc8bebabd27f94eb87d278a38d6a292183f6b473ce`

```dockerfile
```

-	Layers:
	-	`sha256:62c7cd819c5dd97ff517bb3baaab1da5a78d7fbf161de33ec9e96a142ab39a89`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 2.3 MB (2281874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801a09bb3467020196a76bc15ad49a4568bd3079f387e4a563934d3f562014e4`  
		Last Modified: Wed, 11 Mar 2026 19:18:35 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:a34f4faef125d2c1c0b7bd866ca0e3132e10cbc6cd2656b7556a2f267618a1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd2a7233616b14025152fae14adbf8d1fc10e410271edbcbf38eeea4d8f413`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:29:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:46 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:02 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:02 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:02 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88f57d04c7cfe5bb1217bad3e3ff16c30aea89aaade4ec661e53853315a02b`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 1.3 MB (1287310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447bad7b66208f8e935f58d734a53f366f3d6017c5a21abe67c4dd2540f77efb`  
		Last Modified: Wed, 11 Mar 2026 18:31:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dd3c17eee9b3bf39cca9d43f8ff495a7c75199811b65bda5f566afbe968fe`  
		Last Modified: Wed, 11 Mar 2026 18:31:56 GMT  
		Size: 37.7 MB (37661725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00ce345593bb8166503f9a71eeb0eec086b76f9b8ee5d85378d6ce7384165d`  
		Last Modified: Wed, 11 Mar 2026 18:31:55 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d889071b4c31131058eb1717f21630ae829bf20236346853191378472378`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 6.0 MB (6025573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd2386539996dd7ecbb76d8338b4e6ba89be42afd48f6e7f4ee160816220458`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e088c0c3706d7a1de6a2a99084988cb91ba507a308c257bb4e2d242023049df`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13c7afe2833b7e6653f6d520c277980f2e7a7621d992f45dc898511516b52c`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2f589f391f45d80df48ea7b5a8d3ba4a2f836763858f99aa95b3ab3e934cf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f93cc26b17337c0c4f8bdd44ea80516d4fb2bb69783f1696fbf270c18371647`

```dockerfile
```

-	Layers:
	-	`sha256:ba093f17127866de97e95fda615ecbac913309fe75b394d315796d3e2ca85a12`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 2.3 MB (2278790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b5868101a72b0da8c025457d3c4d4e1e55a5296194e5614c043c2c4593900f`  
		Last Modified: Wed, 11 Mar 2026 19:15:10 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de8d3ad6ce1849bf7b5f28006b9212783ef94e4561909d461485a8fc1d8257ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81019590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52803c668efdfed3a0b2398ea8ef2d6dfe238fc97d6e040701d543478b16aa51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:41:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:45:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:45:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:45:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:45:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:45:49 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:22:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:22:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:22:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:22:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:22:18 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:22:18 GMT
USER fluent
# Wed, 11 Mar 2026 19:22:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:22:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bba5358e3f378909e4c0a9cb9af69228f3108fd67a587461fccd3158cb37a6`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 1.3 MB (1309516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bde25b75aac9ba75f7885fbf7286727e870ee78b380c72bc612e409b3f55ce`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928678f951f229519de045ee3851c120dd40d5a36fe1846396e5695cfd5f76c`  
		Last Modified: Wed, 11 Mar 2026 18:46:07 GMT  
		Size: 39.5 MB (39531725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b362d31236d551dffe973f43a7c056cf3d2c5be3d482402a299b46c47d7bbde`  
		Last Modified: Wed, 11 Mar 2026 18:46:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca75c809c185b8b9b3af8851c647e673b0c586e1a1b9afc4085e682cdda7a10`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 6.6 MB (6575733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf00919f179c5e952b990fdaee3167ae0855465c1648e9d6ce0dbb6254aa0c4`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b58f73d83f66b53787162bd9f95f7898ac610e24cda3db51a3bd3222d7806`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc55a1d404e92beb7cc18af679e3b12fd3567c6e4e86adda49137e2f24657aa7`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e134ec73a0dfba5d8cb13f30e4967ab90a3cbccb35389ee43f15b5e8b9d994a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777a754e5615e3f977cb9a52c9c13ac48bd2fde7739a3cec265f9fcd8900344`

```dockerfile
```

-	Layers:
	-	`sha256:895467fd95e7f9047a1b753596a06673f51c2442449f6a0ea05847c089380b8c`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 2.3 MB (2285137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebe8cc4e199aa617ed31aabf514d168691d23c17158c4343019e5025a4f5c47`  
		Last Modified: Wed, 11 Mar 2026 19:22:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:15272769816a339589731725f28014f3cf73e0416f3f0d3afd2ac0dbfb6a95b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3375b66a23ddd0134dfa3c5f5af79b3e2c54f6f5cbcf892481165aa944ff24c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 11 Mar 2026 18:30:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:33:30 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:33:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:33:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:33:30 GMT
CMD ["irb"]
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 11 Mar 2026 19:15:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 11 Mar 2026 19:15:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Mar 2026 19:15:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 11 Mar 2026 19:15:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 11 Mar 2026 19:15:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 11 Mar 2026 19:15:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 11 Mar 2026 19:15:44 GMT
USER fluent
# Wed, 11 Mar 2026 19:15:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 11 Mar 2026 19:15:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2330c467e1931fe73b76bbfce21eb00bbeb1b3408d0f700032ddcb64bb358b`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 1.3 MB (1294488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342513ff2afeeee15c2a6131bc1f9b6bda0e30048d575aa73c13abe3642f4ac4`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096e51e12f56f8972511878c2bdd53785b95467ddc2431a3ed08203e984dfb2`  
		Last Modified: Wed, 11 Mar 2026 18:33:47 GMT  
		Size: 39.2 MB (39205804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c44d6373d7f22f1af2eea10934cea9eef1965e287d8d54f607bda53e16f41`  
		Last Modified: Wed, 11 Mar 2026 18:33:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059721229294da070222585983b257cd6ca81f01a46688fb93366f12f193c09`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 6.4 MB (6429931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff45129a091c48baccc63e67d8f470f5b5c610992ac341d2ca285e35ef3965`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf75ab18f67fb4f9382c309c081e6dbc0fcc15822f4b2fbc758b6db88843aec`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9056a71b599985194f6a6956b6a3879d3c1dd3eb967f2daefff034e1c312f8`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:71504d474cab676e050e9baa575e5eb76234b6a52da2e426ba13b5bd4a2d05ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a78d1b92735b8fbf7a02be684de548f50814027e99dce875d8f8a819f2cc9`

```dockerfile
```

-	Layers:
	-	`sha256:f02789c7eaf625e4c19a111f65e5d6fbe7d3cc7f4fdb8f430a2480298891066d`  
		Last Modified: Wed, 11 Mar 2026 19:15:58 GMT  
		Size: 2.3 MB (2283047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a433fca29ae7cbd3a34d6df5ae84cc11f5dbda5e3bb534023f73842d62a6bb19`  
		Last Modified: Wed, 11 Mar 2026 19:15:57 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
