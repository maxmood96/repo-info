## `redmine:latest`

```console
$ docker pull redmine@sha256:eb12e013e6bb3b8e691e00e8713982088e12747323a07d4e08b9323d6a7af6a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:d6983446453a1bed4d476866483a284da56adae5974e63844824bf5d1bb52a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260399231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ce1ce27a33138bc9a29a996dfafb526b91b0502ace4448f6e6961534256639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Mon, 08 Jun 2026 22:39:41 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:40:14 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:40:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:40:14 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:40:14 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:40:14 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:40:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:40:14 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:40:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:40:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:40:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:40:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 22:41:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 22:41:10 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 22:41:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 22:41:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 22:41:10 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 22:41:10 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:6abde11642f9443036395e822acdc821ed36a4cf7140ae63d2f24761a6091426`  
		Last Modified: Mon, 08 Jun 2026 22:41:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ccfd7b276b61c2679a98dedcfb56d46d1b5dc264417eb3c46b17f3b0824d9`  
		Last Modified: Mon, 08 Jun 2026 22:41:29 GMT  
		Size: 110.3 MB (110331273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1efc61dc42717bf79ce5cacf3f3c6a7dc565adf7838c445e5c18ac8d80fde`  
		Last Modified: Mon, 08 Jun 2026 22:41:26 GMT  
		Size: 951.1 KB (951135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ca0098400632212a3ee26213a1574163c8b06daa8eb425948ec46672f92891`  
		Last Modified: Mon, 08 Jun 2026 22:41:26 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728b1f754031e6501ff5ee438d439dd971aae56e73d89845d8a7ae5711a8f24`  
		Last Modified: Mon, 08 Jun 2026 22:41:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3f56618091fff4ce293d5ba10ab51d2a905c81c2ee95a6ea7d0b7b58c6baa`  
		Last Modified: Mon, 08 Jun 2026 22:41:28 GMT  
		Size: 4.1 MB (4149094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cea174e31c6f080b4a76c78db4c7695e640ee2f26e009454ed0d7faf95f54c3`  
		Last Modified: Mon, 08 Jun 2026 22:41:30 GMT  
		Size: 71.8 MB (71776572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8d4d65265caf04157f51c348aab1720d153451043323c6634c4f4e6bb7798c`  
		Last Modified: Mon, 08 Jun 2026 22:41:29 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:9a2494c89ea05e62be6daa5b74ba478ca9aaf44696ecc54efbaf3464821a6867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 KB (41685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c3a6985f2fbed611369375322f8c3412d35c1497a522ed956e0ef7dd931aad`

```dockerfile
```

-	Layers:
	-	`sha256:b1a81585077eb1edf184a45bc19816174f3a9c61e180a4b9e2a326b830ddbb8c`  
		Last Modified: Mon, 08 Jun 2026 22:41:26 GMT  
		Size: 41.7 KB (41685 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:e06035e627f402c7413d497ab7c213a295979777507c1561684adf810cdb4435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264971558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4485959cfac80bbc2357b815aaaae99e639fa424072fbfd730457e419dd91c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Wed, 20 May 2026 01:50:54 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 20 May 2026 01:51:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:51:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 01:51:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 01:51:50 GMT
ENV RAILS_ENV=production
# Wed, 20 May 2026 01:51:50 GMT
WORKDIR /usr/src/redmine
# Wed, 20 May 2026 01:51:50 GMT
ENV HOME=/home/redmine
# Wed, 20 May 2026 01:51:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 20 May 2026 01:51:50 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 20 May 2026 01:51:50 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 20 May 2026 01:51:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 20 May 2026 01:51:50 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 20 May 2026 01:51:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 20 May 2026 01:53:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 01:53:28 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 May 2026 01:53:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 20 May 2026 01:53:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 May 2026 01:53:28 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 20 May 2026 01:53:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:17c783b1b8c1f744dbfe865502d74fafe7a993686b289d455eb6e94cd3f7b8d8`  
		Last Modified: Wed, 20 May 2026 01:53:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d55b11ca0514d20a1521ca2b8ec7ef6989b3da77666021d54d994aa008995`  
		Last Modified: Wed, 20 May 2026 01:53:48 GMT  
		Size: 106.0 MB (105972432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c378546bb0bc9d1ffbb8df552a173ed1062224cbaa329550ff092c91d1faf0e9`  
		Last Modified: Wed, 20 May 2026 01:53:44 GMT  
		Size: 919.8 KB (919815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf135291a2153f27f53a903cd6fe6d3fc3ed231262859f84da3e5e63712763db`  
		Last Modified: Wed, 20 May 2026 01:53:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d45a4cf75fb659e38dee64d2592264a4b0b0660f6c39f9af5fe12518fb5c2`  
		Last Modified: Wed, 20 May 2026 01:53:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5888b1b6dbc79e41414ade0cdc40cefa16670efdaf06476f0dc8ad7ab489d5d6`  
		Last Modified: Wed, 20 May 2026 01:53:44 GMT  
		Size: 4.1 MB (4149082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f163a27ae9c315d91c2d32ce3c002ef4636d9882451de0cb906e6bf24fd8a3f`  
		Last Modified: Wed, 20 May 2026 01:53:48 GMT  
		Size: 86.8 MB (86784275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5b7ac851015278b1f6816e428e61f56165f9452178be240a0c9b1b11e4592a`  
		Last Modified: Wed, 20 May 2026 01:53:45 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:6fcd24011cd03766f2b3f67f898ad3cb913db35c347bffca0965a90638973954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d39ad92dda344ec12891296c526493d0b52c6441de07e3d72fab93aa53bf147`

```dockerfile
```

-	Layers:
	-	`sha256:834ca6a066d904838ead5aca0652d1faa55f9e3517aea22c8e2c30ea6c2f8792`  
		Last Modified: Wed, 20 May 2026 01:53:44 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:bb925b1c8baf245da7a1a800b592cefb6c5bf7e7615af32b09b5254203257d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257958390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff17bc5bf58452b423f5c45ad404a84555cdc836a7ac8bc69f00303ec49ddfa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Mon, 08 Jun 2026 22:39:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:40:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:40:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:40:23 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:40:23 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:40:23 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:40:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:40:23 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:40:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:40:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:40:23 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:40:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 22:41:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 22:41:47 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 22:41:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 22:41:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 22:41:48 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 22:41:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:7c093503070a57cc54bcfe97a92693f1b3b1c839b799f167469b02f10f2b4de5`  
		Last Modified: Mon, 08 Jun 2026 22:42:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad7440abc86e832325f79b9d6a9c12b2265c92ed9550334f76a1ac2d3b2d735`  
		Last Modified: Mon, 08 Jun 2026 22:42:04 GMT  
		Size: 101.0 MB (101036424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2638eaca94aa71d9af66c4f4efc00226433f4763e1731c1c4529cd642c1be1c2`  
		Last Modified: Mon, 08 Jun 2026 22:42:01 GMT  
		Size: 916.4 KB (916377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6744952d811f803af37f2ddd2de1945fc41641b8cba77407b302911b9000f854`  
		Last Modified: Mon, 08 Jun 2026 22:42:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5480ebb517d0ebd53cb385c6dd6c9974053614dbc127400431a6795e46172e85`  
		Last Modified: Mon, 08 Jun 2026 22:42:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c99bf43d8437ce02190572b055bfcdfde4cb4b65984f22810403454d930bc2`  
		Last Modified: Mon, 08 Jun 2026 22:42:03 GMT  
		Size: 4.1 MB (4149088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0914c5e597388d1abbe1095869122d53c1eb8246571b9d9351aacfd1bf303`  
		Last Modified: Mon, 08 Jun 2026 22:42:05 GMT  
		Size: 86.6 MB (86627845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a44531c82d3b4b02df5f767aec4cbf509541bb3cfecf3146b036ca354e4a7`  
		Last Modified: Mon, 08 Jun 2026 22:42:04 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:60c50744f21b8273f6c8054c5dfd2a760ad1ef89f3da3e7ffe846f7a0dba5c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 KB (41862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f397cc10a67ecf1d6b1f992674c81cd4f1852f1c91288ebda642f82aacc35`

```dockerfile
```

-	Layers:
	-	`sha256:5957c31a0655690a523a48ea12adb1c655f7295df582d8f4988362e12c692a9d`  
		Last Modified: Mon, 08 Jun 2026 22:42:01 GMT  
		Size: 41.9 KB (41862 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:6af854b349b5859e2d05264373e363c2256af7080a10dc03dc91080839fbeabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258864782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778e7d8481710e040e178423f9bd9ff3a6a0877c454907489c0e34e5ec5a8aa8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Mon, 08 Jun 2026 22:38:54 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:39:29 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:39:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:39:29 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:39:29 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:39:29 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:39:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:39:29 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:39:29 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:39:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:39:29 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:39:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 22:40:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 22:40:34 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 22:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 22:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 22:40:34 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 22:40:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:6e61dc5e286d0a36336ac4cd75fb9b389700afd4831aa1ce6aae9234b8f03d9c`  
		Last Modified: Mon, 08 Jun 2026 22:40:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cca340e3e8a8105ea76f09915f51deaf3274bf405dea3203c1581754714c84`  
		Last Modified: Mon, 08 Jun 2026 22:40:53 GMT  
		Size: 108.7 MB (108739644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead8ec22c97722bb37554b7a8f86f8257ae99e004ed8c20fb663ea8b2bae8eb`  
		Last Modified: Mon, 08 Jun 2026 22:40:50 GMT  
		Size: 904.4 KB (904380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dced613424d6157472c8aebb1f71e097a2a2519bb373475d044dd9ef9927a8ee`  
		Last Modified: Mon, 08 Jun 2026 22:40:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667eae49bc87cf9e74e8c087b4a1d350b41938c89af459fc0ee7ae00dce5cc5`  
		Last Modified: Mon, 08 Jun 2026 22:40:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0612384d6d450f208b164285cc0e1d943ec6cc4db877dd2f09a6d9dc24b14`  
		Last Modified: Mon, 08 Jun 2026 22:40:51 GMT  
		Size: 4.1 MB (4149092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e6c633c71c2eb760e0b9348e85c9befb1c515231ceffa7d5de1850a776b7d5`  
		Last Modified: Mon, 08 Jun 2026 22:40:54 GMT  
		Size: 71.6 MB (71584918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b76085f6eeaeb41502098e8ec1f148deeaa15c2d5accf17ac05e26ee2f0152`  
		Last Modified: Mon, 08 Jun 2026 22:40:52 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:484130297bf612b4756d43e1b41a304aca996418b7a484462fef662f95a83416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 KB (41912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60765228a070978860f8f2a7d0954122d598cc6ef1f9f11e409486cc8d3b11f`

```dockerfile
```

-	Layers:
	-	`sha256:3550f030b5f3e620ecc1608f5876041c258677955ca1d869be253b843a512935`  
		Last Modified: Mon, 08 Jun 2026 22:40:50 GMT  
		Size: 41.9 KB (41912 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:833a4ee4c37a0261388abb1f78c3b0cb26e39e729e5fe1dd194df80bc5ade5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277239883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6933928947c150b569bb90e51db90b464e6ac8ad43427c8a0d28068756158d17`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Mon, 08 Jun 2026 22:39:00 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:39:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:39:40 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:39:40 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:39:40 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:39:40 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:39:40 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:39:40 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:39:40 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:39:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:39:40 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:39:42 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 22:41:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 22:41:17 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 22:41:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 22:41:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 22:41:17 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 22:41:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:4a4917c161879ed6df874e532ddcd8b19dbd16c9cedaadb7f6bf94176ab473db`  
		Last Modified: Mon, 08 Jun 2026 22:41:33 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e77c92da8baab7d97891308f9e683d459aca6a215f6bc872c5263f63d6af1`  
		Last Modified: Mon, 08 Jun 2026 22:41:38 GMT  
		Size: 112.9 MB (112863356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72354ce3628c656bfa67d6e47f5abe91ffaaaca3af590277f7808927c0d81dc0`  
		Last Modified: Mon, 08 Jun 2026 22:41:33 GMT  
		Size: 919.7 KB (919740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0574cdc366bd9e56481c41c7753dead8acafc9ac1db129ba9c50a5b69468954`  
		Last Modified: Mon, 08 Jun 2026 22:41:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8f7e399b46f6c4cc2addb9dc9240c24d8701a0adcd26c7f85bf96e6fd7270`  
		Last Modified: Mon, 08 Jun 2026 22:41:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d0bf57e84d41cc118bb0737ac6a5533dc021b6f91a1b64eda9a7a2fb5e1b88`  
		Last Modified: Mon, 08 Jun 2026 22:41:35 GMT  
		Size: 4.1 MB (4149084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516a11afd73258d74fe2893cae5e6db6a2ea6fea5cc0efdfa570e5c47eede08`  
		Last Modified: Mon, 08 Jun 2026 22:41:40 GMT  
		Size: 89.1 MB (89058453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c9f3991ab92e18f7c71a760ac595fe450a18da86cc85993499d81e37d6b3d0`  
		Last Modified: Mon, 08 Jun 2026 22:41:36 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:354c717511b1750eeb5cd9b752540b8a5d9041d4f3ccb61dc6ee3ae8ddb70a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba366d423b5f9c5ce71d83a6331c2d882f83cfdd70ce6aebbf6d1c2d31e0d8c`

```dockerfile
```

-	Layers:
	-	`sha256:5ea9fb2320a7a9ca58044748045928cf49e7fccfe1878838917a84b2d989d24b`  
		Last Modified: Mon, 08 Jun 2026 22:41:33 GMT  
		Size: 41.6 KB (41623 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:0172ac43c0edacc8ee25999a55b867029efb0c0b3276b7776f462fa6a21e687b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301010614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86909a769d0697e31a1f40e769443db760c5e1844ff9baf2d7b02d8f6bd21a8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Mon, 08 Jun 2026 22:38:08 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:39:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:40:09 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:40:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:40:09 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:40:10 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:40:10 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:40:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:40:11 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:40:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:40:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:40:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:40:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 22:44:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 22:44:38 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 22:44:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 22:44:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 22:44:40 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 22:44:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:fecd13d102611b936c6d81697c8464e8803566946e9d00fd15fc2dc7bc67cd62`  
		Last Modified: Mon, 08 Jun 2026 22:45:14 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af93502ea90430ceaf5fcfc95e83a1acb43744f353adb566eb8eb1af183d0c78`  
		Last Modified: Mon, 08 Jun 2026 22:45:17 GMT  
		Size: 117.8 MB (117819737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1413bb4e361c35511be123d24d0d94f7d869611706596964a0ff88e521c5635b`  
		Last Modified: Mon, 08 Jun 2026 22:45:14 GMT  
		Size: 910.3 KB (910311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf70ddb3ce63c53e4191638ae0b67f3f712017cc220d55eee1436725618512f`  
		Last Modified: Mon, 08 Jun 2026 22:45:14 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e49d7d20fca443a3059d0d35aa462824b93ae6397240c83fbce73a2543b45`  
		Last Modified: Mon, 08 Jun 2026 22:45:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d63c8d5c6694c97eb8bf24ce9a5bc9967be2666d50663f41e1e3d4afaac70a`  
		Last Modified: Mon, 08 Jun 2026 22:45:15 GMT  
		Size: 4.1 MB (4149086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9127ec0fe2912481fe6dc015b7b04e0d2a898426b291e29f8aa9a6aaa9aba952`  
		Last Modified: Mon, 08 Jun 2026 22:45:20 GMT  
		Size: 103.7 MB (103683923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9573b487f41e2bb7a4f8dfa0452a819041515173e2b5815fd6f874a953d80479`  
		Last Modified: Mon, 08 Jun 2026 22:43:47 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:77dd3bc19d939f87ba8153f7f15229706f2427b0eb35aadf8d297f8abc236c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 KB (41765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f69b1f1cf755e9c240001d7131f43fddf2ab6c698655e9b23a4a7b18ec00796`

```dockerfile
```

-	Layers:
	-	`sha256:90ec48fa09a7b772ca9078e7e2d13ff9c9c3f751c2a9747e5007777906f2db09`  
		Last Modified: Mon, 08 Jun 2026 22:45:14 GMT  
		Size: 41.8 KB (41765 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; riscv64

```console
$ docker pull redmine@sha256:071fd5c6c1de2700842882361c44a9da9fe2addfa38a22b81cf70ac80ede7e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284514944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a6236c32d8f5ab726b74be008401eb9360600473666f58c77f1a880fc8c41f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 16:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 22 May 2026 16:12:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 22 May 2026 18:17:19 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 18:17:19 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 22 May 2026 18:17:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 22 May 2026 18:17:19 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 22 May 2026 18:17:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 22 May 2026 18:17:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 22 May 2026 18:17:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 22 May 2026 18:17:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2026 18:17:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 22 May 2026 18:17:20 GMT
CMD ["irb"]
# Mon, 08 Jun 2026 22:38:36 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:42:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:43:25 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:43:25 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:43:25 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:43:25 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:43:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:43:25 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:43:25 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:43:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:43:25 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:43:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 23:52:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 23:52:17 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 23:52:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 23:52:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 23:52:18 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 23:52:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442b04c9da1292886476145d93860b6a1fec8086abf6d0eb1f0dd86ba31aed43`  
		Last Modified: Fri, 22 May 2026 18:18:53 GMT  
		Size: 1.2 MB (1249161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526a2f03e04f5f90750611759524891735b98119191f0d5f8f471722ce2b4448`  
		Last Modified: Fri, 22 May 2026 18:18:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c47939c633c88d05bd876da3e178c93eefa4a35c0dd28cf8bfb7ba19574c0c`  
		Last Modified: Fri, 22 May 2026 18:18:59 GMT  
		Size: 38.0 MB (37957533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f135619c7a579e0bf00494dfdb26029e2be226128f9adea434f1470d16076640`  
		Last Modified: Fri, 22 May 2026 18:18:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ff7c30f91b889cc4a473130ebded8b59cfd8bcb433b44890a19faa3f486e5`  
		Last Modified: Mon, 08 Jun 2026 23:55:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11b3e1af66b91995dbe13bcde77c0b969344b5d79373c61d44be043645390ff`  
		Last Modified: Mon, 08 Jun 2026 23:55:41 GMT  
		Size: 107.6 MB (107595182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8d71d4634e19e26344e96c255a0da0723ae361aae16a8e39f259d96cf8f535`  
		Last Modified: Mon, 08 Jun 2026 23:55:12 GMT  
		Size: 897.7 KB (897653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a313830310aa09197fbf3b3e490be873460011581e950c00310165720b219fed`  
		Last Modified: Mon, 08 Jun 2026 23:55:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660c5c62d775dcb718372ebe0c58b0052f53eeb0755cb2fee0b3d5154a0ae23f`  
		Last Modified: Mon, 08 Jun 2026 23:55:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2750d8109aa4bc67a9393868a7704a546a7c83d9ccff552b0e273796ddeb6d`  
		Last Modified: Mon, 08 Jun 2026 23:55:14 GMT  
		Size: 4.1 MB (4149086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb5ec83c24a93afcf6f740e01f00fe4c3d19a9407176a099eb48ab8bd6a9e4b`  
		Last Modified: Mon, 08 Jun 2026 23:55:43 GMT  
		Size: 104.4 MB (104384608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c905f571f4359dce53246d1cf40fe6ed8585ab8f262ad31782ec62d5667f986`  
		Last Modified: Mon, 08 Jun 2026 23:55:15 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:621f1e33d76a3554c8a0e8f964c9304fca2d8b5ff56257547d249fafad54e5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 KB (41764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c01422e9f1378660227f1a8a9331733fe159512002e93e1a17c60a22ab8bc4c`

```dockerfile
```

-	Layers:
	-	`sha256:3de5639c0ed11d205e68e1d0ef7a7f955f252e4999a7d675b2332440025f2c88`  
		Last Modified: Mon, 08 Jun 2026 23:55:11 GMT  
		Size: 41.8 KB (41764 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:8d6b5abb3198c529e43d2ea474b58503d7248d0b213dd5b5044e35dda9e0d60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288835281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32893d11edb3636d5da390e7fc93a4fddc37e26140cc6bacd2f5ffba0be9c8af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Mon, 08 Jun 2026 22:38:04 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 08 Jun 2026 22:38:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata-legacy 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:38:50 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Jun 2026 22:38:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Jun 2026 22:38:50 GMT
ENV RAILS_ENV=production
# Mon, 08 Jun 2026 22:38:50 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Jun 2026 22:38:50 GMT
ENV HOME=/home/redmine
# Mon, 08 Jun 2026 22:38:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Jun 2026 22:38:50 GMT
ENV REDMINE_VERSION=6.1.2
# Mon, 08 Jun 2026 22:38:50 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Mon, 08 Jun 2026 22:38:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Mon, 08 Jun 2026 22:38:50 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Jun 2026 22:38:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Jun 2026 22:42:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	gosu redmine bundle exec rake time:zones:all | grep -q 'Kyiv' # buildkit
# Mon, 08 Jun 2026 22:42:22 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Jun 2026 22:42:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Jun 2026 22:42:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 22:42:22 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Jun 2026 22:42:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:662a1d3d78d99c056a2b7d1b2845a67e57497d0a3ca2e988f28523af05629d67`  
		Last Modified: Mon, 08 Jun 2026 22:42:10 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544ccd80de4df36d454a2967a9ba9f34d85e004aa79352fe14098094d616c77e`  
		Last Modified: Mon, 08 Jun 2026 22:42:49 GMT  
		Size: 111.1 MB (111146124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a58c845d722ea332e488d08428e9c6a1da328d0facd20e53d16596fd6ddb01`  
		Last Modified: Mon, 08 Jun 2026 22:42:47 GMT  
		Size: 923.6 KB (923604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5003d2b9d461adf4075dc3b8b17e3d9807ffee232605b3a0f52ff99bc9f87855`  
		Last Modified: Mon, 08 Jun 2026 22:42:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d1a77f77e1e9c80ed571fcbc44128b24b4716b7844cc539c7bddca3c4008a`  
		Last Modified: Mon, 08 Jun 2026 22:42:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17447874e12bbdea5f17080173cfaf1eda67c9f93e3c9f043ca216a70277db71`  
		Last Modified: Mon, 08 Jun 2026 22:42:47 GMT  
		Size: 4.1 MB (4149085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15491700b920f90bc2cf2dcc318585cc2e489f5b981a5f014376f8d00a30b82f`  
		Last Modified: Mon, 08 Jun 2026 22:42:50 GMT  
		Size: 102.3 MB (102263669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adb662cc45436833b07b0c4a2fef954f1b52b674116beb64774c6d38d2a1af`  
		Last Modified: Mon, 08 Jun 2026 22:42:48 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:e7f221bfeee54a769c8cb8c9ef346f4a9af497e1b93549cd93437fe39fa07fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 KB (41687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dec643be4747c7f625f8cae7b4c30b56be659d311621f39d3b427fc92f496f7`

```dockerfile
```

-	Layers:
	-	`sha256:e7cada716681d2c233a3c9e564116418403d0331d86a7b56c0eb15f817df94ca`  
		Last Modified: Mon, 08 Jun 2026 22:42:47 GMT  
		Size: 41.7 KB (41687 bytes)  
		MIME: application/vnd.in-toto+json
