## `redmine:6-trixie`

```console
$ docker pull redmine@sha256:06d9b68be90679c86018901783e94d469da9473b6ebe2e5f1774bc9530e9ce0d
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

### `redmine:6-trixie` - linux; amd64

```console
$ docker pull redmine@sha256:8a2cf86c1916d6255d1ceaec372dcdbd764262900a5803ee3ca241a384583183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260094419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9573beb0caf1851908af6566660ebbf667ff907fadbbbd2a0b1c5a6ea6770c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:21:07 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 20:21:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:21:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:21:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:21:39 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 20:21:39 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 20:21:39 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 20:21:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 20:21:39 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 20:21:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 20:21:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 20:21:39 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 20:21:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 20:22:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:22:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 20:22:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 20:22:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:22:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b8a2d53e1878ae694f70e310c83f27ab5df5da96806c1e2fdc6352f43aebae`  
		Last Modified: Tue, 24 Feb 2026 20:22:41 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ede8cd28070f9d412fa33ef1517ee3b5077ea9e9d02c134e07b670f51f93bc`  
		Last Modified: Tue, 24 Feb 2026 20:22:44 GMT  
		Size: 110.1 MB (110138090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bc17769cc098170a895cdd5d8b6e7b9c724079d938bf1779f3cf9f320a3e63`  
		Last Modified: Tue, 24 Feb 2026 20:22:41 GMT  
		Size: 949.9 KB (949899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488329facfb69da0f03e9697cc51d7a69e1bdc7931040644f2ae863d3ab9759a`  
		Last Modified: Tue, 24 Feb 2026 20:22:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b7ac3f7790137fefb2f472f211f3e6e49c02999fce4a2b53f69cb4f89ab68`  
		Last Modified: Tue, 24 Feb 2026 20:22:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24f55146d9998b10cd62c4fe35bcff4c92403aae0532c96b2a5c86e7b7d6e3`  
		Last Modified: Tue, 24 Feb 2026 20:22:43 GMT  
		Size: 4.1 MB (4145346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cfed016543d2ced8560cfd0913d26dec8c935f4a6df525d22b1bb95321f555`  
		Last Modified: Tue, 24 Feb 2026 20:22:45 GMT  
		Size: 71.7 MB (71686517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1905ccb3b4e21d50d9326f250dac0278ef16a14c20b06b9ba99679dbda4e5f77`  
		Last Modified: Tue, 24 Feb 2026 20:22:44 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:0560a5d726c82da3c8a3682afb72d3db6234039c61d6dd3123e7a3a41300e04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa510033809ce4fd91014b126ac1e4b43d21062b5b76e2c0f58f5ca44e128f3`

```dockerfile
```

-	Layers:
	-	`sha256:aec27b4ce01cfb64a92b1828302837f1bd718c57f40f9f1dfde3d7c8468f5881`  
		Last Modified: Tue, 24 Feb 2026 20:22:41 GMT  
		Size: 41.3 KB (41311 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:8bf0015e215b0c779bdad2912380a7dd590669b7058d05b2f3a6c2abd6dcc40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264790059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776f6432ccec60173a76c0c84add27b74c844fad95599e54a3e8ec2bfb28c06c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:53:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 21:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:54:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:54:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:54:04 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 21:54:04 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 21:54:04 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 21:54:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 21:54:04 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 21:54:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 21:54:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 21:54:04 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 21:54:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 21:55:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 21:55:41 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 21:55:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 21:55:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:55:41 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 21:55:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5042366f94de29073ce684685c999b4d7e243285977e968b2adacd5378c49ad`  
		Last Modified: Tue, 24 Feb 2026 21:55:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c591e0a224889fe4a20016eecad7ffa46232d358ba4a4c67818803ba8e8b77e3`  
		Last Modified: Tue, 24 Feb 2026 21:55:58 GMT  
		Size: 105.9 MB (105934341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdbf7134bd5ab5de9a0c87ef265a71a9f0742396473a67d6cc0954aad05810b`  
		Last Modified: Tue, 24 Feb 2026 21:55:55 GMT  
		Size: 919.6 KB (919558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a1d3740475a3da310966b77d2dcd89fc40b4df34a3a7dbd12b6650844caa00`  
		Last Modified: Tue, 24 Feb 2026 21:55:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9091401997d031cb93c97896b96b44c4eab9bbea514c84edae42f901d748f3a`  
		Last Modified: Tue, 24 Feb 2026 21:55:56 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88bcaecb6718d93aef78ae4160dc90fc10aa3901fe84a5c911083e6694824c`  
		Last Modified: Tue, 24 Feb 2026 21:55:56 GMT  
		Size: 4.1 MB (4145359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802f4e9ba485ca1fba665cd41851aa7d4b1dce836677df2125bd602045476532`  
		Last Modified: Tue, 24 Feb 2026 21:55:59 GMT  
		Size: 86.7 MB (86669839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749a6b1b279662a37267c88d727cec7764e18ead881b4048a46851e375e83417`  
		Last Modified: Tue, 24 Feb 2026 21:55:57 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:fcb228ae9161e2583dc27fb0f9b4e65eb10eb340207b887b642f2271d98af03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4550b46b731286f72f74147b04942c1e29a7f6169924f851beee57b4c32439d`

```dockerfile
```

-	Layers:
	-	`sha256:c28376d63eb76dcca7abc011fd04bf302f6b9a1fc35aae5d92d54145c97b625e`  
		Last Modified: Tue, 24 Feb 2026 21:55:55 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:d91181c21f44dd2da616008e0754bcac333de9a644a5d067633f9b5996d92503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257655144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d74f7123f3aa821a27ae7185107e6c8c738afb0131326d2a3792688d081b25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:58:07 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 21:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:58:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:58:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:58:50 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 21:58:50 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 21:58:50 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 21:58:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 21:58:50 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 21:58:50 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 21:58:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 21:58:50 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 21:58:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 22:00:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 22:00:14 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 22:00:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 22:00:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:14 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 22:00:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00df85cfda1aa9720465ff011e0e4123fb140dd0ac80fc357cb7288bb46e65c`  
		Last Modified: Tue, 24 Feb 2026 22:00:28 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2598dafbba95f211fada4533112a3d5a5423459d872f8d1f14a7c803c19d0c72`  
		Last Modified: Tue, 24 Feb 2026 22:00:39 GMT  
		Size: 100.8 MB (100836984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1360d08efbba494cf33cbbe1dbc6fa1f8ea16a7f1e6d103f718bd57da7105f4e`  
		Last Modified: Tue, 24 Feb 2026 22:00:30 GMT  
		Size: 915.5 KB (915499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cf7c17ab2cd7995c56aad72a40968b489c9d1f324d2000853784a45b8322ad`  
		Last Modified: Tue, 24 Feb 2026 22:00:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616fed78d82f3b6d6633a7dec58cfa208dbe7b26bb8151b4461e259ae3cee0d`  
		Last Modified: Tue, 24 Feb 2026 22:00:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51080d495129f9c069209041e39e7ceaf6d924a5286240792c88e9de4cc418de`  
		Last Modified: Tue, 24 Feb 2026 22:00:36 GMT  
		Size: 4.1 MB (4145355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d01fbaf1a4076d8e7737af2a418c365543b4e5c6ef8d27ff9ac148dc0591ac9`  
		Last Modified: Tue, 24 Feb 2026 22:00:41 GMT  
		Size: 86.5 MB (86535481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfe078c4bcbb171a1adabe50dcc6d77de477555b843cd5e2d037082a91c949a`  
		Last Modified: Tue, 24 Feb 2026 22:00:38 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:1743bc74058bcb21a36bc2dc2830cc61a44d6e6ae7de734d6cb85522a11dd189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303de646e38b8f6fc41ee97737f61ff7345fc2f54047aec3b4c7afdc30393c0e`

```dockerfile
```

-	Layers:
	-	`sha256:8d51e207d212d77ae5cfb783f2169f2cb5c72f28a9e967e5959df4bdab7d353c`  
		Last Modified: Tue, 24 Feb 2026 22:00:29 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:3605cf2f265a2bb20bf2a6ffe2a172b6e2371eb052c49f2bc84719d4b8fcc34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258583086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a06f0d0b69157353028147f07f732b9967e20f3c16d05359f94a8e25d75ce6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:36:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 21:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:37:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 21:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 21:37:25 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 21:37:25 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 21:37:25 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 21:37:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 21:37:25 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 21:37:25 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 21:37:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 21:37:25 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 21:37:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 21:38:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 21:38:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 21:38:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 21:38:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 21:38:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b83b2c3e768b682da948e52831afda1d4d6f5de42cb889bdda1219c755fd337`  
		Last Modified: Tue, 24 Feb 2026 21:38:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7e219d46b7a466920516b85921e2dbf6a5a1ae6e4b16074beb786556be86a8`  
		Last Modified: Tue, 24 Feb 2026 21:38:48 GMT  
		Size: 108.6 MB (108563163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b33c071aa9ad4dd019f08e85923efd2f9147ceaadd181980a1fd9f407e6e2`  
		Last Modified: Tue, 24 Feb 2026 21:38:44 GMT  
		Size: 903.4 KB (903390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d9b4822242c7ff2f1986a19cb153f122ded8f5630a2a1192e4be2c4b47f38`  
		Last Modified: Tue, 24 Feb 2026 21:38:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914a8a09aaa3b5010f9aedbf4d07ef19b1eedbd59332a6db1574b0a7fc29b07`  
		Last Modified: Tue, 24 Feb 2026 21:38:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58124f7257c4f60eeb40e5fdddee1e9165e1dd5ea5877b0fb83018f2e17e879d`  
		Last Modified: Tue, 24 Feb 2026 21:38:46 GMT  
		Size: 4.1 MB (4145355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05908d4b6c39e084e06c071da8cf9906c3f658c40fc0d1e4e2e2fbfe29027c`  
		Last Modified: Tue, 24 Feb 2026 21:38:49 GMT  
		Size: 71.5 MB (71491537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c1d9abd2d4247bcc3ee5beb8efbf0a15f86d7f5d3f26565798742fdceb749f`  
		Last Modified: Tue, 24 Feb 2026 21:38:47 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:1df6d4de18473a1d5eb244bf07986b70323d7fa4792bed4eb496c2fca7d146b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3380579387d31d96a612c6591fdada7e543b19a05e360a88d301585513939a3d`

```dockerfile
```

-	Layers:
	-	`sha256:6cf1d7c8c384a7317a29a5756ee104d5632650143286b3eeae4a3ab6cd766bcc`  
		Last Modified: Tue, 24 Feb 2026 21:38:44 GMT  
		Size: 41.5 KB (41539 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; 386

```console
$ docker pull redmine@sha256:5b47756dfc716b63af47bf4946d198230f0162ea225046611beeae60c090e018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276926270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535917aa54d868f592bea8cdd8f4e487a522917654dd602a7fa405f5d3cc9dda`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:12:51 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 24 Feb 2026 20:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:13:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:13:28 GMT
ENV RAILS_ENV=production
# Tue, 24 Feb 2026 20:13:28 GMT
WORKDIR /usr/src/redmine
# Tue, 24 Feb 2026 20:13:28 GMT
ENV HOME=/home/redmine
# Tue, 24 Feb 2026 20:13:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 24 Feb 2026 20:13:28 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 24 Feb 2026 20:13:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 24 Feb 2026 20:13:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 24 Feb 2026 20:13:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 24 Feb 2026 20:13:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 24 Feb 2026 20:14:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 20:14:53 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 24 Feb 2026 20:14:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 20:14:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:53 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 24 Feb 2026 20:14:53 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8939a9d669582da1a72dc8456706b78677c873ea8ded9863c514f3592a7fac0`  
		Last Modified: Tue, 24 Feb 2026 20:15:07 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9fbc392b2ba8355741eb51240b95599f084d53569e64922b9c6abcd8a550ef`  
		Last Modified: Tue, 24 Feb 2026 20:15:10 GMT  
		Size: 112.7 MB (112652287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3722b53491c1de82a88d7a56b67ccfdd3e868467632b2a2c4e0a0c3dfa74875`  
		Last Modified: Tue, 24 Feb 2026 20:15:07 GMT  
		Size: 918.8 KB (918807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e72d6611be03c7b3d96c86b32015651e4f0524fd28f9e585c4cf8a7ae46855`  
		Last Modified: Tue, 24 Feb 2026 20:15:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2bab00bac8009b7288d951da384c1a323be2370502753fe7b1d4a516574ffc`  
		Last Modified: Tue, 24 Feb 2026 20:15:08 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d67ed74f858655833dc8239770283db01f87c75faefde4d6ab6c5380bbf8d4f`  
		Last Modified: Tue, 24 Feb 2026 20:15:08 GMT  
		Size: 4.1 MB (4145350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd176e8c12828766b75954afc03cb57c33099f44480c9ac719b0ebcff5385c7`  
		Last Modified: Tue, 24 Feb 2026 20:15:11 GMT  
		Size: 89.0 MB (88962895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dfdd63cd14606b5f725e8a9be62ed536112fd10c2e5ca24cf225996dd5ee91`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:e5dbbe88f14835d39567fe0ed7e6b3584a54b14e99d3a7432a08d613453a9ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290c162797d217b8ce1c8f968f62c517a58434f2fe166c07c7a0a5e57084936`

```dockerfile
```

-	Layers:
	-	`sha256:08ec8b20e060f3523fe377a1dd90a6476d77a559701d865faca9e0ab5c2e53de`  
		Last Modified: Tue, 24 Feb 2026 20:15:07 GMT  
		Size: 41.2 KB (41249 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:c5167cde3f38746a309ee60a506d941dc31e12607c5825f784b17a7498d26b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300698697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc99e657be65ea1192669c912c2b5a3bbedff283102f8088b1718889fd64e448`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 01:07:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:22:28 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:22:28 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:22:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:22:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:22:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:22:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:22:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:22:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:22:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:22:28 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 05:53:27 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 25 Feb 2026 05:54:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 05:55:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 25 Feb 2026 05:55:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 25 Feb 2026 05:55:21 GMT
ENV RAILS_ENV=production
# Wed, 25 Feb 2026 05:55:23 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Feb 2026 05:55:23 GMT
ENV HOME=/home/redmine
# Wed, 25 Feb 2026 05:55:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 25 Feb 2026 05:55:24 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 25 Feb 2026 05:55:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 25 Feb 2026 05:55:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 25 Feb 2026 05:55:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 25 Feb 2026 05:55:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 25 Feb 2026 06:00:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Feb 2026 06:00:19 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Feb 2026 06:00:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 25 Feb 2026 06:00:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Feb 2026 06:00:19 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 25 Feb 2026 06:00:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82b23e0d804a54b0e580f49e08c88d0a8935ae62df49531fc9a104bb84b9f56`  
		Last Modified: Wed, 25 Feb 2026 01:12:30 GMT  
		Size: 1.3 MB (1309532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1cef8d0cefd8f2d25bdc6163c892c81ca58a783806319e902958aa9850e547`  
		Last Modified: Wed, 25 Feb 2026 01:12:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e23cdd06877150cb84c5c348f9d7debeb3c0f2aec932099ced8ae1a42b614`  
		Last Modified: Wed, 25 Feb 2026 01:22:49 GMT  
		Size: 39.5 MB (39519578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd719a37b914fa050fc9424a34152138cfab3428df113ea40133dfa158a98701`  
		Last Modified: Wed, 25 Feb 2026 01:22:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefc2608c82bfa0430c2a6221c27ad87f26ac081c8602f5c404246f67c797224`  
		Last Modified: Wed, 25 Feb 2026 06:00:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b8f0ac771a1113e19879700dcda30cbaf7d2fc29beb86ade39cef88b449ff9`  
		Last Modified: Wed, 25 Feb 2026 06:00:55 GMT  
		Size: 117.6 MB (117629379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb06f872fa6a0d06e60d6c5feb36224f0feed6fb2db62a49acde64ec0fef9d72`  
		Last Modified: Wed, 25 Feb 2026 06:00:57 GMT  
		Size: 909.6 KB (909572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00205e42b0327d20c70db299ac03d437f86951e8603cdfb116c1eba62a95a0ba`  
		Last Modified: Wed, 25 Feb 2026 06:00:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9943d275e4409305df85950742883649c6f71a673ff431d2f2dbb7d2b75807`  
		Last Modified: Wed, 25 Feb 2026 06:00:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9da0dd59a3d986c062e2d81fb09fac7311db839f2792442e34740671b8787`  
		Last Modified: Wed, 25 Feb 2026 06:00:58 GMT  
		Size: 4.1 MB (4145344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82955d13706a2f56aef4eefbb3b5cf1aaabd5a6bce2001460cd1cd7a222ef0ee`  
		Last Modified: Wed, 25 Feb 2026 06:01:02 GMT  
		Size: 103.6 MB (103580958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421150094eb8202b989414c726b67ef639a95bda0aebb800fea1e75f499c6542`  
		Last Modified: Wed, 25 Feb 2026 06:00:59 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:f0b2ad1f058354eecaeb0b0e5f2f50012f1f715b25c4880df1d180ce40f38718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49b56e06dbba593a2988f556ed9c94c5ddd02e1947f83bca165cc130dceb059`

```dockerfile
```

-	Layers:
	-	`sha256:40b590806ec87ed2311f5cdbbefccd05b4b4e269a0571c5a8c618e980e374927`  
		Last Modified: Wed, 25 Feb 2026 06:00:56 GMT  
		Size: 41.4 KB (41392 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:241a312e30ef9f00b9e677865c30aacd849801346a50c106efb45ca1efa4a631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284162986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a905b8b0d7efe293a58783a1d3d32448cf49d8470861bcb4153150e43e48210a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 16:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 27 Feb 2026 16:25:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sun, 01 Mar 2026 14:18:48 GMT
ENV LANG=C.UTF-8
# Sun, 01 Mar 2026 14:18:48 GMT
ENV RUBY_VERSION=3.4.8
# Sun, 01 Mar 2026 14:18:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Sun, 01 Mar 2026 14:18:48 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Sun, 01 Mar 2026 14:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sun, 01 Mar 2026 14:18:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 01 Mar 2026 14:18:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 01 Mar 2026 14:18:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 01 Mar 2026 14:18:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sun, 01 Mar 2026 14:18:49 GMT
CMD ["irb"]
# Wed, 04 Mar 2026 11:54:22 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 04 Mar 2026 11:58:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Mar 2026 11:59:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 04 Mar 2026 11:59:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 04 Mar 2026 11:59:38 GMT
ENV RAILS_ENV=production
# Wed, 04 Mar 2026 11:59:38 GMT
WORKDIR /usr/src/redmine
# Wed, 04 Mar 2026 11:59:38 GMT
ENV HOME=/home/redmine
# Wed, 04 Mar 2026 11:59:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 04 Mar 2026 11:59:39 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 04 Mar 2026 11:59:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 04 Mar 2026 11:59:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 04 Mar 2026 11:59:39 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 04 Mar 2026 11:59:44 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 04 Mar 2026 13:08:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 04 Mar 2026 13:08:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 04 Mar 2026 13:08:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Mar 2026 13:08:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Mar 2026 13:08:46 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 04 Mar 2026 13:08:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ccfdbc7e183d1e89d27ebcc0447326b7c9bdb062f24585abeb2ae79c02b01c`  
		Last Modified: Fri, 27 Feb 2026 18:25:00 GMT  
		Size: 1.2 MB (1247707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd7d0cf8e2448471c93c58b5ae1b57b6236514865c5d7f1066e6adc6bb54913`  
		Last Modified: Fri, 27 Feb 2026 18:25:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d70ea358de9c944948c401449f2a2846ca102bc13e89f413790d4c8592a7ea`  
		Last Modified: Sun, 01 Mar 2026 14:20:27 GMT  
		Size: 38.0 MB (37966139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0c744d7acfa56d308fbd46039121ce2e7c6e82ebbf26ce413e3e15458e7259`  
		Last Modified: Sun, 01 Mar 2026 14:20:21 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd96e2a72f975da6c860cb36fce50d58cf228650f9ce2ae8aee9ca054e377de`  
		Last Modified: Wed, 04 Mar 2026 13:11:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e88dcec8a8cf8ac4ec22f7add6cfa594424cd1d0df4f4d606005c50dd8a8e5`  
		Last Modified: Wed, 04 Mar 2026 13:12:09 GMT  
		Size: 107.4 MB (107403562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f742d8184586bcbf01bb3040c1f19b2bfb133ecd64f3072235b6f270afa4f277`  
		Last Modified: Wed, 04 Mar 2026 13:11:40 GMT  
		Size: 896.6 KB (896594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa0170b5c9db81eef7fe4e4957d302984ca1c9cae6a1d8b1f66edba8b872496`  
		Last Modified: Wed, 04 Mar 2026 13:11:40 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10c6f395dfc90805721f4cfdbd8668639eb70d9fda90248c4dadcf12755a4f4`  
		Last Modified: Wed, 04 Mar 2026 13:11:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca4613baec461f1a7068ae78d9c6aa537c966307f020a5dadfb89ed02253e9f`  
		Last Modified: Wed, 04 Mar 2026 13:11:43 GMT  
		Size: 4.1 MB (4145355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65cab797f6ce4979052675143636ed4e18f8558a3b757f6144d1d2124f359`  
		Last Modified: Wed, 04 Mar 2026 13:12:11 GMT  
		Size: 104.2 MB (104223090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815d1ec30820f34d5e0afdbd18c26e271a1b6c6071f8ca5029dfb46ae823c91e`  
		Last Modified: Wed, 04 Mar 2026 13:11:44 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:4d651f640b92034a9c33ed260ae352bf4767e8c4ed04ec946785e0bcc8dd6cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8115529dac7459a1194833a4e01cd981907c83b93f8f964776de434ab6f67d85`

```dockerfile
```

-	Layers:
	-	`sha256:bd6b757cc2d2b71e828ffbe50f4f7c07bc43571df6c9761ffb3bd682d3c8ce41`  
		Last Modified: Wed, 04 Mar 2026 13:11:40 GMT  
		Size: 41.4 KB (41390 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; s390x

```console
$ docker pull redmine@sha256:04b999ad71dff55cd2494290dd0479bee767e38748efbd72fe3339a63805d9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288501887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b20380a6d6f7e69fdcfd1efa1b1df94768c1b9edf75ec00996fe145a882b01a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:02:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:32:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:32:11 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:38:00 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 25 Feb 2026 02:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:39:31 GMT
ENV GOSU_VERSION=1.19
# Wed, 25 Feb 2026 02:39:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 25 Feb 2026 02:39:31 GMT
ENV RAILS_ENV=production
# Wed, 25 Feb 2026 02:39:31 GMT
WORKDIR /usr/src/redmine
# Wed, 25 Feb 2026 02:39:31 GMT
ENV HOME=/home/redmine
# Wed, 25 Feb 2026 02:39:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 25 Feb 2026 02:39:31 GMT
ENV REDMINE_VERSION=6.1.1
# Wed, 25 Feb 2026 02:39:31 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Wed, 25 Feb 2026 02:39:31 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Wed, 25 Feb 2026 02:39:31 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 25 Feb 2026 02:39:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 25 Feb 2026 02:43:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Feb 2026 02:43:27 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 25 Feb 2026 02:43:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 25 Feb 2026 02:43:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Feb 2026 02:43:28 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 25 Feb 2026 02:43:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4914443d3c4184b2c3ca5f7f265c77f7783c5fe40f5ff77daa520ded4b0a2c`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 1.3 MB (1294517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def914eff926e8e33e8d2ea6891e3ece82a54502d942da1cf995fac0cf626932`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fad6ee4d8be5d7dbfd8551d2a5d070571e5d13c57cfc9d2618d596970e34c`  
		Last Modified: Wed, 25 Feb 2026 01:32:41 GMT  
		Size: 39.2 MB (39192544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56a57c12ad1160bc0ee7c91d149dab3f7a2a858afd9771d4f967a14a4533a`  
		Last Modified: Wed, 25 Feb 2026 01:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe21518ec3af348b6570a800276c60e55e54f4e3d01df96fec187cb15265da15`  
		Last Modified: Wed, 25 Feb 2026 02:43:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51985fced297d33fc128fab25ae083e4b2ea93610b876a4ae9206bdb53ecd519`  
		Last Modified: Wed, 25 Feb 2026 02:43:59 GMT  
		Size: 111.0 MB (110965552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b499df551888c396237b910ac188b130f5f2097255e188a4faef99b4c48774`  
		Last Modified: Wed, 25 Feb 2026 02:43:57 GMT  
		Size: 923.6 KB (923587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b012b93790f0062fcdecb2625b8ae32599d499ab6c5926fd444a2c2f598f0`  
		Last Modified: Wed, 25 Feb 2026 02:43:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b32815d8c3059a4f3cdd9e177bd3306f646e9ace0640c7079ab94867a43197`  
		Last Modified: Wed, 25 Feb 2026 02:43:58 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12c478be3b553995422debe87b7ee009c49b39186f1ebfc8b9b383b6bb20eea`  
		Last Modified: Wed, 25 Feb 2026 02:43:58 GMT  
		Size: 4.1 MB (4145353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd91c3bd95806e27a942f1b8e866c06b690ec42e35ab9f4d0fc3c8b03299a866`  
		Last Modified: Wed, 25 Feb 2026 02:44:01 GMT  
		Size: 102.1 MB (102138038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbd11c67d1b51b05836a7fd55df3a63088d942ddc301e346f0b5ec2f524f56a`  
		Last Modified: Wed, 25 Feb 2026 02:43:59 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:920bc93db1bacb9aeffb5d5afc9d864374584cf98b6409641fe148f3d42692f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d6352aba681876f529cfdba3b3604b8e9ff9ba9febe3e1bc666b9762050572`

```dockerfile
```

-	Layers:
	-	`sha256:6cc4b6630412a35613bf106c8154f51ca435776ff792710dbed1b43da0596c95`  
		Last Modified: Wed, 25 Feb 2026 02:43:57 GMT  
		Size: 41.3 KB (41313 bytes)  
		MIME: application/vnd.in-toto+json
