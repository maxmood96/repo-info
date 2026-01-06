## `redmine:trixie`

```console
$ docker pull redmine@sha256:44e08dc3804ffbc0d6d9e7ba27c1b7b645df779d0d48f71195e2b37039d1ef67
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

### `redmine:trixie` - linux; amd64

```console
$ docker pull redmine@sha256:e4175ede6cb9faeac99bcd7f897d0986383531c366d158cdc5de5b7f465a7b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255602456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899806668556715939c9a7e1715d05b0907bd8e43b1d64bca9cf011a7355bc87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:45:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:45:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:47:48 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 00:47:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:47:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:47:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:47:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:47:48 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:47:48 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:25:29 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:26:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:26:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:26:01 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:26:01 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:26:01 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:26:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:26:01 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:26:01 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:26:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:26:01 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:26:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:26:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:26:42 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:26:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:26:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:26:42 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:26:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3f82d8b2b84a490177071ffba31720bfb49acb0e43e2a998e116c8f9e38177`  
		Last Modified: Tue, 30 Dec 2025 00:48:01 GMT  
		Size: 1.3 MB (1279418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a703fb352b369c2d889461725f817dc3db510690d710f2dcb1e3154aea02273`  
		Last Modified: Tue, 30 Dec 2025 00:48:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972213005d369f582dce1669fa13c5846a2835ad44233803accb7576a2b960d`  
		Last Modified: Tue, 30 Dec 2025 00:48:05 GMT  
		Size: 42.1 MB (42112330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac039e63a1ea58452045c2b17ecf741eacaa97e6c965346c7d0879b4604332c`  
		Last Modified: Tue, 30 Dec 2025 00:48:01 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d2055d85bbbb2d794983a6bce74b278f8e7aaa252d3af03b62218b784faec7`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f26d2ab0eceb92337923f5c7bb7407da51bba2d0b283932bdd033f7cab81c0a`  
		Last Modified: Tue, 06 Jan 2026 18:27:20 GMT  
		Size: 110.1 MB (110148647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc51c35cfd1f7a65662256e9553915e845c9e2221e02e6c86d9c304cd84e52a`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 949.7 KB (949729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4381ba37c2fe405097ed3d1b15d783302b244c8d8133d071e060d7eef4d32055`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9f7141e37dee058af24220b64852cd99c58f7d325d1ad8a9e1d4bcea6035f`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef42647d3efacbd70204e2a91b5509c8eb0efa7fb12e5ef43836adfb9128d2d3`  
		Last Modified: Tue, 06 Jan 2026 18:27:07 GMT  
		Size: 4.1 MB (4145354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02455dcac1475781d6a0561e0347a509ac72b199a31669db774f1f1785dd7eac`  
		Last Modified: Tue, 06 Jan 2026 18:27:14 GMT  
		Size: 67.2 MB (67186327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15920089af947ddebee6673ef4fe352a19bef95e8b4ea692ae79847842e74e1a`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:004b4928a943766b7067ab38dab335ba9a1bbb371da1467310bfea4eb46d209e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331a6160947ea40e4ec777c67851186e4440eb6734bf2f0567e2105357c11c6f`

```dockerfile
```

-	Layers:
	-	`sha256:a3933e3a05e8cd97cba3b89ed07c66797271514b685092946521e49ea9b8bb25`  
		Last Modified: Tue, 06 Jan 2026 20:52:42 GMT  
		Size: 41.3 KB (41312 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:72470796a6b6c08828731092fefbd651be594032f4df1d61f15a64ce95726ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260323700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744a6cbe64c893a0a745a58a4f21c86b0896efbdc49f154b9c212fffa1b8cbdb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:08:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:11:54 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:11:54 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 01:11:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 01:11:54 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 01:11:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:11:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:11:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:11:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:11:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:11:54 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:25:58 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:26:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:26:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:26:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:26:57 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:26:57 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:26:57 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:26:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:26:57 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:26:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:26:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:26:57 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:27:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:28:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:28:35 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:28:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:28:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:28:35 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:28:35 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e4b1c9b816c636def9d490041218bfbdd3f37dc813c37db0d2b8b4ede4a098`  
		Last Modified: Tue, 30 Dec 2025 01:12:10 GMT  
		Size: 1.3 MB (1263028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578fd90120971b5e505555ba7e6f8f98c0f8b564a5e006c969c8d8926472b614`  
		Last Modified: Tue, 30 Dec 2025 01:12:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d243f50f6bbb9337b25d8788ff3b34a73d494de9f239c2147873c5dada3cde`  
		Last Modified: Tue, 30 Dec 2025 01:12:13 GMT  
		Size: 37.9 MB (37906154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1ef86045bbf0427399d82d8f27ed604a6cbb1c4063360e16ec7995d425532`  
		Last Modified: Tue, 30 Dec 2025 01:12:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa40af1e24846c7b14ac1b8a81cb0f1c5b3ee01fc493959f8ede28af1f25c09`  
		Last Modified: Tue, 06 Jan 2026 18:29:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e54db1d666761d73b05c9c1bef8012953a7df6f5cb1f5a93a384ffe37ba4c8a`  
		Last Modified: Tue, 06 Jan 2026 18:29:10 GMT  
		Size: 105.9 MB (105932566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2791c2da7aa40ab22d47c357ba6e0d907171dbef4d29253f2708775be21f6cb`  
		Last Modified: Tue, 06 Jan 2026 18:29:02 GMT  
		Size: 919.4 KB (919374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0623f2f143c841096a615313c4c47c28b38a2855e2d21931ad51ad022349ec3`  
		Last Modified: Tue, 06 Jan 2026 18:29:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e73d25543141897d2a89d1104d8b10d0a2b1950ad3ca85dd32fa24ce995de6a`  
		Last Modified: Tue, 06 Jan 2026 18:29:02 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482d6bc49cfdd4dcbefcc0d25c1523d849e09827cf85f17a9b1e4ac733337a`  
		Last Modified: Tue, 06 Jan 2026 18:29:03 GMT  
		Size: 4.1 MB (4145348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6017f38ca2aeb6744dea43c20bad5ccab74eb5017a3e1dfafa474ae99169b2`  
		Last Modified: Tue, 06 Jan 2026 18:29:09 GMT  
		Size: 82.2 MB (82208967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60edb2b895fcd1222106d3b00ef46b976924b57fb969e9abc1add33f9528f891`  
		Last Modified: Tue, 06 Jan 2026 18:29:03 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:88bcad71faadff08ec7505b0ef33ea7c93a003119205dca80c24bd386cb00cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d49ffe11da33c6ae63d9a34a579d14a9561a6901e00a149cb016b23f2c74eb`

```dockerfile
```

-	Layers:
	-	`sha256:d26ec7a036be8b1a539dd9c654f9f30b477ee5ffe7a88bc825745c22d8ce71a7`  
		Last Modified: Tue, 06 Jan 2026 20:52:45 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:4303fc1a164d90c0a4110941c4d230e1026d011499eecb90345dfb8e95dcc07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253177908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0149b0299fd40f25cbf8593e2142228901f18ba123b2335704e334bbea6088a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:42:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:45:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:45:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 01:45:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 01:45:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 01:45:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:45:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:45:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:45:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:45:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:45:03 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:26:28 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:27:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:27:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:27:08 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:27:08 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:27:08 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:27:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:27:08 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:27:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:27:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:27:08 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:27:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:28:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:28:26 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:28:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:28:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:28:26 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:28:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb07a57ef2e8915a5c72f33caef6b28df50d1e9339b009d924f19660f1bb47d`  
		Last Modified: Tue, 30 Dec 2025 01:45:19 GMT  
		Size: 1.2 MB (1236528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71818343477bfbb99d507df41c1619d159f6858a5abe20dff04fdf9c4921ec8`  
		Last Modified: Tue, 30 Dec 2025 01:45:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3617adf354ec63e6bbb5e6e0db0b8a51d0b7cc913d9718644c3f0763232f5649`  
		Last Modified: Tue, 30 Dec 2025 01:45:28 GMT  
		Size: 37.8 MB (37767052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174446788b782c20a045c265edf3b0f78849133e356bc434447451025192747`  
		Last Modified: Tue, 30 Dec 2025 01:45:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272b569184c2166e11acff1d9c1fce09bf88cc40c7ec1d2d5e2530e7eaf0c476`  
		Last Modified: Tue, 06 Jan 2026 18:28:50 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0981566484248044420dbaf51a36992d19faed43b1e0457a0786c0a3fbf118b1`  
		Last Modified: Tue, 06 Jan 2026 18:28:57 GMT  
		Size: 100.8 MB (100843386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b87401883c33d17f02a1d9b7ee90f0b8dd4c576ad5ee9e2486bebb5b67a30d1`  
		Last Modified: Tue, 06 Jan 2026 18:28:50 GMT  
		Size: 915.3 KB (915314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3658f625a0ac5639878813dbfdbf9c5860a602aaa92d0b13d821dfaed96cf7`  
		Last Modified: Tue, 06 Jan 2026 18:28:50 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ff1cf19a816d076e8839ecce13c3e9320be234a84bad72333f1ee2795b2d7f`  
		Last Modified: Tue, 06 Jan 2026 18:28:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51363fcafb4b027475783f6405ec4c7faf7c34972a96d84740c480b534f77419`  
		Last Modified: Tue, 06 Jan 2026 18:28:51 GMT  
		Size: 4.1 MB (4145344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025becdeb279095dc20ecf18bbfab3d2a332693c47205cb1de935c10826b1298`  
		Last Modified: Tue, 06 Jan 2026 18:28:56 GMT  
		Size: 82.1 MB (82056165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96410d4f9fba10d07edc5365d503abf391e197ffbe693c5cd8394e2d93701a93`  
		Last Modified: Tue, 06 Jan 2026 18:28:50 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:3ca23f43cbf5db3a776cf261cc943541b52135f33a3cb495f832ed8a45f8529d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2769d25da318f937737d46e20dcf8e76f0f9b94722e05c77dba6fd83fd947e0b`

```dockerfile
```

-	Layers:
	-	`sha256:6a67b3f393fe89724bba65307b4694722b33bc2c59655c06044465f54b4a4d7b`  
		Last Modified: Tue, 06 Jan 2026 20:52:48 GMT  
		Size: 41.5 KB (41488 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:1d8e838ffc335f4613319030ab068af530d9b54e4a3c0c22b7409e2d5aee15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254231095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c7415c461535f91ddd4b78a6fc2101660f0acab437ef8018c209eaa881e362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:50:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:50:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:52:39 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:52:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 00:52:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 00:52:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 00:52:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:52:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:52:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:52:39 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:25:52 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:26:27 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:26:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:26:27 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:26:27 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:26:27 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:26:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:26:28 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:26:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:26:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:26:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:26:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:27:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:27:11 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:27:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:27:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:27:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:27:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3183fdb7fc98c15e70d3b6d9ba67ae6e41e2aa929413236db750c4521df9fb53`  
		Last Modified: Tue, 30 Dec 2025 00:52:57 GMT  
		Size: 1.3 MB (1261691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d46ba2a1fdc8652bfd68b538943821d6b4274161d6f8081895d1f283191b89`  
		Last Modified: Tue, 30 Dec 2025 00:52:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c227e52765cf93de91a72f103ea2acfb301c19b45d79948be43d259df5832`  
		Last Modified: Tue, 30 Dec 2025 00:53:02 GMT  
		Size: 42.1 MB (42073709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf44f0cf00ebed6323c8b8b816a67b124012b8033e58a22342dd419e6f09ae4`  
		Last Modified: Tue, 30 Dec 2025 00:52:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7464604a1e82de1dbbb2dafa27c3ac496a6628eb34dbbb545753d0c412a7e87b`  
		Last Modified: Tue, 06 Jan 2026 18:27:36 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bfdb090e0f6a57715a7ec71ffa21ad153dc47a24ce4e845836b109be708191`  
		Last Modified: Tue, 06 Jan 2026 18:27:46 GMT  
		Size: 108.6 MB (108561412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaa281611d906dc4845098f781dd34b4f36070e9e0a114ef1c5c84ffbf8b3ce`  
		Last Modified: Tue, 06 Jan 2026 18:27:37 GMT  
		Size: 903.2 KB (903178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd703abac598e163e6b68d924cd6730d3695f282439fa760d1d8da31f6b80ac`  
		Last Modified: Tue, 06 Jan 2026 18:27:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f99644a2bf4e0ca60292e0d34705a6b9eddd7e723d777578a1568f7e75f5a97`  
		Last Modified: Tue, 06 Jan 2026 18:27:37 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e061826b3d02eaf2af62453c91ca5f1b5bb649e54c89927a81cb5b8eb05459`  
		Last Modified: Tue, 06 Jan 2026 18:27:37 GMT  
		Size: 4.1 MB (4145346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b49c9de1ac73547d1363fc2b701027936d5a8bca749fb58c3f9baa30488793`  
		Last Modified: Tue, 06 Jan 2026 18:27:40 GMT  
		Size: 67.1 MB (67143008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47781b48d55e66a7d341f5806fda79ce5ba9c4aaf529a7aa45b14de85f0f1ef2`  
		Last Modified: Tue, 06 Jan 2026 18:27:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:5c4c8c0f65b0743a43a353f866a3144d71eb5b734f657bd0f08ced22b9126869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f5875da816ff59c1bf9ea3f8e4a281ad07c2ae1044620b68bd202e0d726aa7`

```dockerfile
```

-	Layers:
	-	`sha256:4752347005303eff958bed338a8fd3d1f8dc1170aaad618d45065cbc9235983d`  
		Last Modified: Tue, 06 Jan 2026 20:52:51 GMT  
		Size: 41.5 KB (41539 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; 386

```console
$ docker pull redmine@sha256:d9bf3fbe527ffcaf4c1a251c8f343945145dd16b31901c50f8ff9c704a8953b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272529627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4acccb6cfacf0917602c08e274729d172382ad982942c0d995cfc1634f1b6e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:12:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:15:13 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:15:13 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 00:15:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 00:15:13 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 00:15:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:15:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:15:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:15:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:15:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:15:13 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:25:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:26:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:26:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:26:18 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:26:18 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:26:18 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:26:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:26:18 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:26:18 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:26:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:26:18 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:26:21 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:27:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:27:49 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:27:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:27:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:27:49 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:27:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975753064198344e755679c6bca60bcbb08ca2e56f29acb58807e3f8edb6c9a0`  
		Last Modified: Tue, 30 Dec 2025 00:15:26 GMT  
		Size: 1.3 MB (1287251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f10a931458cc9a7130fb6bb718473e910babdacba6ef90673a5b81379580285`  
		Last Modified: Tue, 30 Dec 2025 00:15:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc5026ce01a097e7e662cf895ff0b46ddc2f99229b0c12cb2d1f20ce6874e0`  
		Last Modified: Tue, 30 Dec 2025 00:15:31 GMT  
		Size: 37.7 MB (37661245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e9981cd50892ee03a4c54ff77a588aa9b71fc0d12abcc2abde2dd9794fbb6`  
		Last Modified: Tue, 30 Dec 2025 00:15:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513921a12248b610b9ff2a70e79fc5ec542e6d92d68e726c719f6691e6ccbab9`  
		Last Modified: Tue, 06 Jan 2026 18:28:15 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2996f73f251c5fd5e735c768a5a387081089aa185db6560c0e943f0896108d43`  
		Last Modified: Tue, 06 Jan 2026 18:28:24 GMT  
		Size: 112.7 MB (112659328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d9538ed98941d648c3a4711401bb6f09ff0442e44e6775340215b26bbb78d8`  
		Last Modified: Tue, 06 Jan 2026 18:28:16 GMT  
		Size: 918.7 KB (918657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05984793c18ed798e6568a2142fe7b4581d2c0d7434d8cd77d827f442335047`  
		Last Modified: Tue, 06 Jan 2026 18:28:15 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1909f19f543c5a30b12ebb1396644f543003769ad182b39f1462c5afa5b01a`  
		Last Modified: Tue, 06 Jan 2026 18:28:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ded8c4691458496370839bc5de2d9f1f2299877b24cf9e90430337babcf8440`  
		Last Modified: Tue, 06 Jan 2026 18:28:16 GMT  
		Size: 4.1 MB (4145345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcec96fbf8d54fc2dd8aa8db64dca6b06e40fb8a0a5a485a819100865f425e05`  
		Last Modified: Tue, 06 Jan 2026 18:28:21 GMT  
		Size: 84.6 MB (84560583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15920089af947ddebee6673ef4fe352a19bef95e8b4ea692ae79847842e74e1a`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:d6da02e9dd903af66009b4c86354e587fe6d974eb8fef3528ef2a316b37dbb9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bffc34bd2fd8be51d74ea942d9ac589e5ec1f7d6f6f134ac0fbfcf6e9a23f0e`

```dockerfile
```

-	Layers:
	-	`sha256:9bf1952aa989141af8af7c0a90f6a66b9c0e2145c77fe2456d263fbc255562cc`  
		Last Modified: Tue, 06 Jan 2026 20:52:58 GMT  
		Size: 41.2 KB (41248 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:8867404ea425e400faeb08b1f4c684a8791c1fea6a0c1c871ecc842eaf4b35c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296009374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5423279c4bfc2f771473030f1b6ac5640e90427336926bf6160a45a44ddbddec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:53:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 18:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:57:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 18:57:58 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:25:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:27:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:27:53 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:27:53 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:27:53 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:27:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:27:53 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:27:53 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:27:53 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:27:53 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:27:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:32:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:32:24 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:32:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:32:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:32:25 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:32:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec427cb0f29aa78b3a35043f5c43e0a07e16cba482febff3fe2087900b8e01`  
		Last Modified: Tue, 30 Dec 2025 18:58:40 GMT  
		Size: 1.3 MB (1309698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119f3f7815c4977fbb7b151b6aaa8cf695081c5e63a241e7e8ccfa7cff83fcb`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841342fbfd6bcc1a592039fcb307930a186477e89093dcc569ddb52f69b663`  
		Last Modified: Tue, 30 Dec 2025 18:58:42 GMT  
		Size: 39.5 MB (39519497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ecf017368e45fae8cb085ed7b4384c0e98da8232a690f0b6c1dffc3a99bb0`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87156e5b4e584ce81107fa3568563974016b6b3096bcf0b7e938e2c740e28667`  
		Last Modified: Tue, 06 Jan 2026 18:33:27 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5de7ac7f79015687bbcbef00e3017dea3f019ac3082921a51276edfea5954d3`  
		Last Modified: Tue, 06 Jan 2026 18:33:41 GMT  
		Size: 117.6 MB (117626973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff82182fe2e5fd5da3b7138ba6c4fe21a889010c367c568906d2acdc8c004493`  
		Last Modified: Tue, 06 Jan 2026 18:33:27 GMT  
		Size: 909.5 KB (909473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baba0743331a00dd1c3acef059c1e97f0c2ab9c7520fdae0e4719f2dde42e18`  
		Last Modified: Tue, 06 Jan 2026 18:33:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a723f708f1c380a232b0704c36eb78a26fbb0029938771b7ccb8526b92ba118`  
		Last Modified: Tue, 06 Jan 2026 18:33:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8202e70a06c3367a48984636daa0b1ea76a03168981e96913972b6a92226661d`  
		Last Modified: Tue, 06 Jan 2026 18:33:27 GMT  
		Size: 4.1 MB (4145349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59fce48885a41fe98313809bb7a1fcc7f02413bcf1355fd0d64b623fa602582`  
		Last Modified: Tue, 06 Jan 2026 18:33:38 GMT  
		Size: 98.9 MB (98897371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95be05adc0f19474aba25eb9c1ee3f6a14110898d2167b42a7fb27379b796881`  
		Last Modified: Tue, 06 Jan 2026 18:33:27 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:e353e0e0db368d8512d6c574735f29c7ff9758410d414832e203b2a5b797f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f20516bfd06ac8c9587fc198b94306000ba113bc83cd414146cd9c1cf60f404`

```dockerfile
```

-	Layers:
	-	`sha256:f426dc7df158b731e332305328b4aebf93e62dd599a04bba1f5fac636f81bc0e`  
		Last Modified: Tue, 06 Jan 2026 20:53:19 GMT  
		Size: 41.4 KB (41390 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:ae51c27a148dcbdabdaca93bd7fcd1a8acd9cd2bc0b022d8ef64193c152bea17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e7fe70acad4688c9615340cd944d65877c17b17e758c7291e1045c559fb145`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 00:48:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 00:48:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 01 Jan 2026 04:56:03 GMT
ENV LANG=C.UTF-8
# Thu, 01 Jan 2026 04:56:03 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 01 Jan 2026 04:56:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 01 Jan 2026 04:56:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 01 Jan 2026 04:56:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 01 Jan 2026 04:56:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 01 Jan 2026 04:56:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 01 Jan 2026 04:56:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 04:56:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 01 Jan 2026 04:56:04 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:26:09 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:31:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:31:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:31:02 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:31:02 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:31:02 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:31:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:31:03 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:31:03 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:31:03 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:31:03 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:31:08 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 19:39:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 19:39:57 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 19:39:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 19:39:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 19:39:58 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 19:39:58 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce77dcf592ef0e38ea136a7a369fefa0b1f7344af06ddda7fe23bdc6137c01`  
		Last Modified: Thu, 01 Jan 2026 02:50:19 GMT  
		Size: 1.2 MB (1247995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c437f0ef83daf3a2b76a2c51d38c272b6e91fed0d67191ae359042c82544b7`  
		Last Modified: Thu, 01 Jan 2026 02:50:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2977af9fcca68aa7b5cadb7dbbc249325f389d4ab5336f0e69b2bebd4084d`  
		Last Modified: Thu, 01 Jan 2026 04:57:54 GMT  
		Size: 38.0 MB (37959847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3b1e9180150c747e70284323b9e0c88519213219606d8faefa73f5572bb411`  
		Last Modified: Thu, 01 Jan 2026 04:57:51 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60375bd93ba2b46bbcab280171cdfe0122209370d48d031e6f2db5cd32cb5f37`  
		Last Modified: Tue, 06 Jan 2026 19:43:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b99cd204d2ea98f0ff3cacfecad6a8663a28cbee74acc164b22e73c5cadd112`  
		Last Modified: Tue, 06 Jan 2026 19:43:41 GMT  
		Size: 107.4 MB (107394120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3cb931d9f10eb683d6eb214133ccc3fd5ccd1f07f1b20d154aa7391b2bec1d`  
		Last Modified: Tue, 06 Jan 2026 19:43:29 GMT  
		Size: 896.4 KB (896371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444169273015f140f9ae2d0777798075f0606780f795ec0e9e8b70d0dfdf6ae4`  
		Last Modified: Tue, 06 Jan 2026 19:43:29 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc013fd95e3a2eb3c072a8bee333ca984b68e47c32b5ece24bcd417414ed20f`  
		Last Modified: Tue, 06 Jan 2026 19:43:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205119f00c1e960dcd40eae0f3c1b4fd44f8aaad6a0429ef37df4608cc9a25d2`  
		Last Modified: Tue, 06 Jan 2026 19:43:30 GMT  
		Size: 4.1 MB (4145343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86970a8b71f7e313373afabf6480486a743f4538d86f661e3e8b0dc2a47139e3`  
		Last Modified: Tue, 06 Jan 2026 19:43:37 GMT  
		Size: 100.1 MB (100052315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47781b48d55e66a7d341f5806fda79ce5ba9c4aaf529a7aa45b14de85f0f1ef2`  
		Last Modified: Tue, 06 Jan 2026 18:27:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:454523a90a290342dfb501407f13842086594665da3cb06b5fca7a41bdd12e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e96bd9dce57308f13095ace50b16dfe8ec5fa2144679da1d10fef0b8d2f6df`

```dockerfile
```

-	Layers:
	-	`sha256:8dc3feb2aa8a92067083f77a4c8c15d1ff485eb9226c74a14582cd2d5c2d4229`  
		Last Modified: Tue, 06 Jan 2026 20:53:22 GMT  
		Size: 41.4 KB (41391 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; s390x

```console
$ docker pull redmine@sha256:6a01b7fc228a7597242cdc6e036395410287257feace9c4a02928d8e3e56a1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283830120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ed6026db78581ba6c8a7ea71992fac3cf1a44e2e1f803a9d77f3f4b52948b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:51:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:51:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:54:32 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:54:32 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 01:54:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 01:54:32 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 01:54:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:54:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:54:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:54:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:54:32 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:54:32 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:25:29 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:25:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:26:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:26:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:26:06 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:26:06 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:26:06 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:26:06 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:26:06 GMT
ENV REDMINE_VERSION=6.1.1
# Tue, 06 Jan 2026 18:26:06 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Tue, 06 Jan 2026 18:26:06 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Tue, 06 Jan 2026 18:26:06 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:26:08 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:28:34 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:28:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:28:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:28:34 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:28:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528b2a04b7b80b3dca8fec03ae0226090a72c259b8b26c3d3a0f00e3a453d44`  
		Last Modified: Tue, 30 Dec 2025 01:54:53 GMT  
		Size: 1.3 MB (1294295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd038b1b9ae71af581e559fd993f6882a7668a8436c8b057e891d7a70de00254`  
		Last Modified: Tue, 30 Dec 2025 01:54:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5450a5305d6d984f587ab8d21fccddc17cf3239699b76c0f998eee48668150`  
		Last Modified: Tue, 30 Dec 2025 01:54:55 GMT  
		Size: 39.2 MB (39190881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e2ba3d00bfb2a08536b2ff4538ae7140a71b541e47e87bd6f679540be9119b`  
		Last Modified: Tue, 30 Dec 2025 01:54:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d2055d85bbbb2d794983a6bce74b278f8e7aaa252d3af03b62218b784faec7`  
		Last Modified: Tue, 06 Jan 2026 18:27:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf13a57fcec082e552e22cef266de267763fdc1de0f3209fd7ae956976ef7c`  
		Last Modified: Tue, 06 Jan 2026 18:29:11 GMT  
		Size: 110.9 MB (110949474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965578e574106147dcd0b1f9435ec6b164c57f830232b7316b7bf6d28409aead`  
		Last Modified: Tue, 06 Jan 2026 18:29:04 GMT  
		Size: 922.4 KB (922385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869a0ccc0f2eb14d6272b9b3888ec2c1b243a1d50d08914ec91b096cdc1cccf8`  
		Last Modified: Tue, 06 Jan 2026 18:28:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ccb68839fd219d0f60f7bbe9352655c4cdc74282350680685cd5b98c7a8126`  
		Last Modified: Tue, 06 Jan 2026 18:28:43 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934b3efeda239b4a79092a254cc53fbf618976f975ab0dcea803c1c5d4bbae33`  
		Last Modified: Tue, 06 Jan 2026 18:29:04 GMT  
		Size: 4.1 MB (4145341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7ab2fa199914716600865fdca42c436f12044ef5d5e2a33a3b6994dae0e30`  
		Last Modified: Tue, 06 Jan 2026 18:29:22 GMT  
		Size: 97.5 MB (97489209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0e3f03c70b96023381f49257ebe6e327a82557f0120044398f631d3a272b7d`  
		Last Modified: Tue, 06 Jan 2026 18:29:04 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:593e71087ec3382310fc47c9f72f842687e36a70e81cedb9812d719fd1ea9457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5ca13e7f0ed21b038455d5a2f3c4032af53af9193fbd752cf76cc22a5efba0`

```dockerfile
```

-	Layers:
	-	`sha256:fe6a5b6f5977b598dd4b15fc5c57ad985f85f2202e12a41987c37663ba28e9ff`  
		Last Modified: Tue, 06 Jan 2026 20:53:25 GMT  
		Size: 41.3 KB (41312 bytes)  
		MIME: application/vnd.in-toto+json
