## `redmine:6-bookworm`

```console
$ docker pull redmine@sha256:a9b58d5104c9fb54f3e2d69cbfa83c5dc0f6fae5a6a2e3e8bc2ad0820ac28816
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `redmine:6-bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:bd85fd8593f2ebbc5eef9db7eff0af8cfa03587bf9fbe5c078346c3c579f7c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272845015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b11cad1396019baf48f88d591339a3a85ca95ca1a90279c831d0452549a06c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:47:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:38 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:38 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:38 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:38 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:21:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 20:21:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:21:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:21:42 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 20:21:43 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 20:21:43 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 20:21:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 20:21:43 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 20:21:43 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 20:21:43 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 20:21:43 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 20:21:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 20:22:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:22:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 20:22:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 20:22:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:22:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb88befb5f2f53e5432a019ab5a95cc3c46678c2c7650e36632bd6a21702b6`  
		Last Modified: Tue, 24 Feb 2026 19:49:48 GMT  
		Size: 3.5 MB (3510200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207ed7b44e67881d6c07074039b591942559392b9e8c4b7b8248a4359aa6042c`  
		Last Modified: Tue, 24 Feb 2026 19:49:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81536c6e24032a0dcc26a970abe2bfb6db767b83ddbe30e4cd3193aac67e57d`  
		Last Modified: Tue, 24 Feb 2026 19:49:49 GMT  
		Size: 41.4 MB (41442974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b72868f68a1e0b41fed086b3caae478eae1931ed44c7d48fc144b5495a2f8`  
		Last Modified: Tue, 24 Feb 2026 19:49:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18e2e9155ddf4dd9da274e5f3b0b8ddf7f606441379ca24fd84e1284369a9f7`  
		Last Modified: Tue, 24 Feb 2026 20:22:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a53075f57f3d3af8ce1d489e38bdd693d6c590b2ff23ead8e9dce71a2e35f`  
		Last Modified: Tue, 24 Feb 2026 20:22:53 GMT  
		Size: 123.1 MB (123143558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c56af16d06875d8f44b8bc4fd484698f7cc172a25ac54168038ada5eb22375d`  
		Last Modified: Tue, 24 Feb 2026 20:22:49 GMT  
		Size: 946.9 KB (946939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252981132f215ee874f3f46286c5295cf5ae2ab42f49b168f844bdd465f3330`  
		Last Modified: Tue, 24 Feb 2026 20:22:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4e4a33a6f9b45e4bc157157e51e74970ffcc8eacb4f09750b53add64c0e18b`  
		Last Modified: Tue, 24 Feb 2026 20:22:41 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b5cb018ca0aab270413e4810f23ebf0acb8eefbd3b48197f3c7f4230446530`  
		Last Modified: Tue, 24 Feb 2026 20:22:50 GMT  
		Size: 4.1 MB (4145349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1692030085e91bce43d7a8782da2588885741b5e8a00b8a8b1b8240fa0d791`  
		Last Modified: Tue, 24 Feb 2026 20:22:53 GMT  
		Size: 71.4 MB (71415602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0de2029e6a420cbc069386c4106552519a7502d09fe73eefc7ad3f9f72ac5a`  
		Last Modified: Tue, 24 Feb 2026 20:22:50 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:910ed8cae34f1baad4fea8c119f36ef8e0d093de4127c765c9ef4648a42745db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fc67b5b0e2d10c803c1ea5f73a25bd082ea77eba474f7d5a436e157a91d7e2`

```dockerfile
```

-	Layers:
	-	`sha256:aa10bce95a082d95303d2b2045d4f8019588809b94ed9d7715c3bf300d06a367`  
		Last Modified: Tue, 24 Feb 2026 20:22:49 GMT  
		Size: 40.6 KB (40572 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:f1709b12e8a9c242bad4d578a9e8b54380e41ef6bb00dfa0e4fdd65bbf91c452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269638859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247219482504b91df9a8836aeab7ec7bb87b25cd4b791c668df8d3546d5169e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:33:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:35:53 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:35:53 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:35:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:35:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:35:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:35:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:35:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:35:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:35:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:35:53 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:36:51 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 21:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:37:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:37:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:37:22 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 21:37:22 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 21:37:22 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 21:37:22 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 21:37:22 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 21:37:22 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 21:37:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 21:37:22 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 21:37:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 21:38:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 21:38:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 21:38:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 21:38:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 21:38:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2a752c1453184fe7809d86ce35c8dc3cdada059232f9ea517b3e31f20251ab`  
		Last Modified: Tue, 24 Feb 2026 20:36:04 GMT  
		Size: 3.3 MB (3341467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84398e683a1f136442cd9a5ba268941b08f3290378d26c51901a9eddbb1964fa`  
		Last Modified: Tue, 24 Feb 2026 20:36:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90460a3b60d9d3ef9445e7e7be4a195eb52b99b25b76d08636d68199295d7c5`  
		Last Modified: Tue, 24 Feb 2026 20:36:05 GMT  
		Size: 41.3 MB (41329529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268f1afb13adef671a9f5d219aa153d8885a96f9a4853fd193306d88e585ec1b`  
		Last Modified: Tue, 24 Feb 2026 20:36:03 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b9933088205d48b87af19ba8b00afe77ba83f1e6d89a6215b2381c7b24d37d`  
		Last Modified: Tue, 24 Feb 2026 21:38:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424eb445f005357c42abee84011d79bca8c3f9b71a4ee559dd20c71c9a765606`  
		Last Modified: Tue, 24 Feb 2026 21:38:36 GMT  
		Size: 120.6 MB (120589951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a4ee874198219b5a1b704f874cf885a631650fa6132c763def2c65d31c4ca`  
		Last Modified: Tue, 24 Feb 2026 21:38:33 GMT  
		Size: 900.1 KB (900084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48bd13c515a09f41edd14ec2d64c5a4588ef33f4421a5fc168e8f5f68473c3f`  
		Last Modified: Tue, 24 Feb 2026 21:38:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379fb8b7961135784dcee77473db3809601a764d0cbe76fe35dc1ba764e8d783`  
		Last Modified: Tue, 24 Feb 2026 21:38:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1213f3579c8852ba833c7389e4862b58ce6e821f576f662620c65a5448a1786`  
		Last Modified: Tue, 24 Feb 2026 21:38:34 GMT  
		Size: 4.1 MB (4145352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6837ad782dc9fc5f82f7eeb7e7b41aebade27b09a425de45fb68693b00e80aa3`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 71.2 MB (71212279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6230c136e0f62c7f43a9e6c94c538d799cd1f0dbd94a4d7fc713cc3260e0bb5`  
		Last Modified: Tue, 24 Feb 2026 21:38:35 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:3f1cb361097c4882eba712849555e7ca11f4fe4417715fbc0cec370e0dc3be12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf3db6c5b73a159c32b6f2b8aaf103dc1cf986d299658fa326c7ab78b138650`

```dockerfile
```

-	Layers:
	-	`sha256:4ee8a1b5dd93739bb6eb21b5b0ffbfea66509f8963ae12b08f4823068b7d441a`  
		Last Modified: Tue, 24 Feb 2026 21:38:33 GMT  
		Size: 40.8 KB (40752 bytes)  
		MIME: application/vnd.in-toto+json
