## `redmine:6-trixie`

```console
$ docker pull redmine@sha256:3a84604c6301902cded3e49883ff44e764ea3a04a447ec504f70aec380f0e454
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
$ docker pull redmine@sha256:220d204d138671665033e1c616b7ce0c248fa3854b07a306bdd62488d3669a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255331381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1c14330caf315492a2d62e520564aeeca66746dfee7c47c40ddc43152ce104`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 20:06:09 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:06:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:06:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:06:44 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:06:44 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:06:44 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:06:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:06:45 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:06:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:06:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:06:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:06:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:07:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:07:28 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:07:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:07:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:07:28 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:07:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:580069b51f71809f43021792cd956aaf2b2101cc6a62f8c1e5dc91cc1da9183f`  
		Last Modified: Thu, 04 Dec 2025 20:08:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bd1a2621f1dd3bee1fb630b6e150692f9d97a68250f9b4cdcdbad8f0558b2d`  
		Last Modified: Thu, 04 Dec 2025 20:08:48 GMT  
		Size: 110.1 MB (110148565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45e2525cc3669343bb09d2b839505668a1f64961743e17eb94f1ba8423bd901`  
		Last Modified: Thu, 04 Dec 2025 20:08:30 GMT  
		Size: 949.8 KB (949818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031bb6dc8fdd9824ab0ed8fb7a95d7636eda1e5c413d751948d442ebc97b020e`  
		Last Modified: Thu, 04 Dec 2025 20:08:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eed095612b7199137d1e8d2be7202ddc6b61392ba1f355804b6f6d2eee8c80`  
		Last Modified: Thu, 04 Dec 2025 20:08:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0cbc843cb17ca4070590b837008271477da28b48d66cc0495eb677b8889588`  
		Last Modified: Thu, 04 Dec 2025 20:08:31 GMT  
		Size: 4.1 MB (4139978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99808116bae3791a312831358ce72cd3b2b163a37541084cb49cb03547333a57`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 66.9 MB (66874342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e40e37579954c4e2a57f3cc2679ea0c002dc4cacfdf87af4d84c713b075743`  
		Last Modified: Thu, 04 Dec 2025 20:08:32 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:dabf7038aa232390d3f749a8654d00e856b31762768e53cf465a686d0e2b3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1480b2cc3ac78c9235014ac35e3ffa5811af0a82dffd9f62b73c6ce73d03113`

```dockerfile
```

-	Layers:
	-	`sha256:69749561c6279b0a642d93bfd07aa40ab6a7452a58a95a2595b131d234d75026`  
		Last Modified: Thu, 04 Dec 2025 23:52:09 GMT  
		Size: 41.3 KB (41312 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:12851f703b714f94cb25b24b1e882e707256165d20d0fc02941f9998ace1b2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260056720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46816388176412b51c5e9102c17c1d341a251d7ac2aba057d5b8b3367855a862`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 19:59:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:00:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:00:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:00:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:00:51 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:00:51 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:00:51 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:00:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:00:51 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:00:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:00:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:00:51 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:00:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:02:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:02:25 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:02:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:02:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:02:25 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:02:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:86bc512d6ff301e46962fae623cb66fb84234d55bccccd0d63cd8fb07d427e49`  
		Last Modified: Thu, 04 Dec 2025 20:02:55 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415168d19692fa07f01da248f1fa323487dabf9c64aac3d7ad63154acdcdbd80`  
		Last Modified: Thu, 04 Dec 2025 20:03:10 GMT  
		Size: 105.9 MB (105932814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e0af01b0c17155579724c38eef11cea911d3b6a58fa470f309c2937db809a`  
		Last Modified: Thu, 04 Dec 2025 20:02:55 GMT  
		Size: 919.4 KB (919370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a409da7e391fdd9346f20e81d983d9028ec8f8b5e89ee3feda5aea4b9b96ac4`  
		Last Modified: Thu, 04 Dec 2025 20:02:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67d98a5eeacbc264515998ddf8ed3f2fef47d2a24fac1d6d5161e3275a5e5f`  
		Last Modified: Thu, 04 Dec 2025 20:02:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2903025f513d2dabe7c6e85970be996579d646f9b41841e14cb58cbeb4e63e18`  
		Last Modified: Thu, 04 Dec 2025 20:02:56 GMT  
		Size: 4.1 MB (4139978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677b1485c4b533014fc89e2e15afd8bd3c9535f1d0452beec691a5e1ee2efb63`  
		Last Modified: Thu, 04 Dec 2025 20:03:05 GMT  
		Size: 81.9 MB (81859086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05a412547bb492cae4752e19143f58153ace186f1b0026f068e397e722a9d52`  
		Last Modified: Thu, 04 Dec 2025 20:02:56 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:9ddea073a6e64b1ae384347adc96ddcae2974266bd777347720cfb7452089243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d217b331f0dc09cc30824456f628e80ac22e515fd87ff035ac107b6ccce74e89`

```dockerfile
```

-	Layers:
	-	`sha256:e6455d0c702c5ef906d992fa1d7b5fdba687d850187671793952840f96b36ddf`  
		Last Modified: Thu, 04 Dec 2025 20:50:47 GMT  
		Size: 41.5 KB (41488 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:36ded30d48535eb6d62a4c284362df4e3425020655e710a2948c60026bbfdae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252934762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2c85f26d4fa678f34157f8bc97af564a359f43b77fe74a94624946eb1ce12f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 20:06:12 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:06:53 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:06:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:06:53 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:06:53 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:06:53 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:06:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:06:53 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:06:53 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:06:53 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:06:53 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:06:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:08:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:08:12 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:08:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:08:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:08:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:08:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:f93f5fa261d09ae47ebf0475f4d24eb834c09126a5cef54c8650df44031b08ee`  
		Last Modified: Thu, 04 Dec 2025 20:08:07 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd25b4ed9a56cbe130e34c137ac51ceebd14a9ca2200900a489e8ad2bbdee8be`  
		Last Modified: Thu, 04 Dec 2025 20:08:43 GMT  
		Size: 100.8 MB (100843609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b84ed42c765dbc8e02112a6f390f17d19ef200c72efa534bf5739020ae5e5a`  
		Last Modified: Thu, 04 Dec 2025 20:08:36 GMT  
		Size: 915.3 KB (915272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a387da9e915d892edc44420e4226b8d1b59610d527f8c7b49b553e0494fb4a`  
		Last Modified: Thu, 04 Dec 2025 20:08:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c26bae9980a5dcc79e9a1f125dd29cf35e509dd2ca2a961fbb72ca2ab3e61c`  
		Last Modified: Thu, 04 Dec 2025 20:08:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251bec11580ee4a0db735ffb9be6d19ed8eb51bf6be2d131b016119ec3041ba4`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 4.1 MB (4139976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7539e0c886b98e408f2515cc2416d8f33fc653ce22ce6c2e21ff7dac0bae60f`  
		Last Modified: Thu, 04 Dec 2025 20:08:49 GMT  
		Size: 81.7 MB (81719489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf76b1135736e499e06798cc66d2c746fbe02fe1627a5cbeb24cf0f224dd49c`  
		Last Modified: Thu, 04 Dec 2025 20:08:36 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:60de3322a1a8b0c24753cb44c6a8dd173fd5d898f32ee37064ec7faed16e21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea89e887b375a65746396987d6b00cc7871f722fdf96ae8de162e8753f145b88`

```dockerfile
```

-	Layers:
	-	`sha256:8f4da81849789d96d3428ee81f0f1f6c24425ac454ca8fa7ddcf94c402b40927`  
		Last Modified: Thu, 04 Dec 2025 23:52:14 GMT  
		Size: 41.5 KB (41488 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:ab9e607e89672d5f0350c8ea06e3688dc263305d3753be864c6daa832f77d267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253969830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30679019290560b7dde3ebfd4441425057af314c396cbb2ad14820aabdb20dfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 20:06:52 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:07:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:07:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:07:28 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:07:28 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:07:28 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:07:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:07:28 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:07:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:07:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:07:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:07:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:08:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:08:11 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:08:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:08:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:08:11 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:08:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:e2d3623f3491da5c7af75b87207a3cee867cc6654827196577f93945d15f9382`  
		Last Modified: Thu, 04 Dec 2025 20:08:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f2a5f6ee2af674cefb822c3c15dbff1afab3647ff51f592bbc53f5f1174541`  
		Last Modified: Thu, 04 Dec 2025 20:08:48 GMT  
		Size: 108.6 MB (108559903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8361369302db4f62fdffb5bc71ea33b2233259de8e4520b7f7e9358b637ec1`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 903.1 KB (903148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9477e238cec942b69f35cc2ac0c4747d5bfee67ff3002e0f02c8c8d071c225a`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40701f7c20ef57fb32b71ce5c3e9568e9dae934d513b8b52ea69df28f0a64b11`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5aa3f989189745838a4a906b31fa085080b9dc2d5fa2fade64073127416a83`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 4.1 MB (4139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a4c44417043bf2ac710c31c7abd67a00d117c3194091a684788d54d74b32c4`  
		Last Modified: Thu, 04 Dec 2025 20:08:43 GMT  
		Size: 66.8 MB (66816682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009b5b0011cb59cd6e276afcd3c587d0fe0d42cf48596c325445767b99bbb24a`  
		Last Modified: Thu, 04 Dec 2025 20:08:37 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:97cac0c4b07aca14e9f16fcfb36e54511795f81e2047314342d56aabe353caf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596ef4cf39b0b16b78cff5b395ae92e5953ae01d7bbc8f3a3735f985ab3cd31a`

```dockerfile
```

-	Layers:
	-	`sha256:5757c51b14fa4aea30a862e81d1283271655b6a30df188f49c6362ef9d5cb7f3`  
		Last Modified: Thu, 04 Dec 2025 23:52:17 GMT  
		Size: 41.5 KB (41539 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; 386

```console
$ docker pull redmine@sha256:aca1c1bf8491f4cba9d8e01d60f771f17d3e30c623c342c684c98c37f0717e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272251808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b899fa9caf48a82ba8b28ebe780f021db601d2d1dd59150c7b8caa56c825d09c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 20:03:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:03:39 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:03:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:03:39 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:03:39 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:03:39 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:03:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:03:39 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:03:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:03:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:03:39 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:03:42 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:05:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:05:02 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:05:02 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:05:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:8f53f5da6b28b65012c95dc4459ae191157a2ff083f7ca37a6d7b1ff645e3ff6`  
		Last Modified: Thu, 04 Dec 2025 20:05:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd8057ca7c2efb5d0563dbdbed368175933c7e2dcac266c5834b9c7f44ce62`  
		Last Modified: Thu, 04 Dec 2025 20:05:41 GMT  
		Size: 112.7 MB (112659513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5952534348dc5a5c1cf22fa782e03a78f6460e5afc351cbeb9dd6f46bf910`  
		Last Modified: Thu, 04 Dec 2025 20:05:30 GMT  
		Size: 918.6 KB (918585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd32d04982d5ca2cd0969d2ceecf58a5ac252fb4741331a4fc56be863eb1764e`  
		Last Modified: Thu, 04 Dec 2025 20:05:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7f0c829b3106f9e73cf71e720d7738db90315dbdb336352ea24c23e656581`  
		Last Modified: Thu, 04 Dec 2025 20:05:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d50768320e98c156ad93ae1e26a0d5ce953e49ddf0890353e054c1f8e2978`  
		Last Modified: Thu, 04 Dec 2025 20:05:31 GMT  
		Size: 4.1 MB (4139975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40e3d5bce6a793c27878c1d928770b3c63e6a7de44eaf2f560f3d111b786a88`  
		Last Modified: Thu, 04 Dec 2025 20:05:39 GMT  
		Size: 84.2 MB (84209090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd713ed2d605e387fff2dfefebb21e9734d2086a3610fb7601c650a3bf091a`  
		Last Modified: Thu, 04 Dec 2025 20:05:30 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:91ec7f487929d2dfd61674106dc7598c5bd9322f957bb527d3bba2a30009c0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2febca7fb0f46f6b6750285cccc4093a2108a2ec2c33395a1b2bfb2e946c8751`

```dockerfile
```

-	Layers:
	-	`sha256:428768ac6181f28f6659ca4b18846592fafa4546aeb5f2985d819dea8599046f`  
		Last Modified: Thu, 04 Dec 2025 20:50:54 GMT  
		Size: 41.2 KB (41250 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:4f1c30cc38815127669a0507225ab3bdb2281256f2eacfa7990620833c90b8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295730005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fe5b403c6d98bcd6cc3caaf9876864327d66cb80c4dff34953253546351a24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 20:14:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:16:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:16:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:16:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:16:56 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:16:57 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:16:57 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:16:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:16:57 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:16:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:16:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:16:57 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:17:01 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:21:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:21:20 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:21:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:21:21 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:21:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:cfcda21f8444201285abd5d858da937f8762f1b9fb2ddfc5035f034278f7b420`  
		Last Modified: Thu, 04 Dec 2025 20:22:27 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c192824c76e9785ab859970ed6319cda2d47d215f838e2be6b02c0549be5ca`  
		Last Modified: Thu, 04 Dec 2025 20:22:38 GMT  
		Size: 117.6 MB (117625810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68339ba5321783a73468789067cd5a7dfb6d4adb4604cb7f49024f2f0a75e05c`  
		Last Modified: Thu, 04 Dec 2025 20:22:27 GMT  
		Size: 909.4 KB (909424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9db469019af9f17d15d1c1c94868bedc7edd1bab6b07c67672e1a128baf3e8`  
		Last Modified: Thu, 04 Dec 2025 20:22:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f9e1f5d368c3595aafbfe6742d01d79df0d77ad3cc051ebee7f705ff2bf33`  
		Last Modified: Thu, 04 Dec 2025 20:22:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5cb6857423e14dd6edeafd483547e84333a73e9a40709ee027c2761637d2cf`  
		Last Modified: Thu, 04 Dec 2025 20:22:27 GMT  
		Size: 4.1 MB (4139980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c140115caaeec49cfd2eaf3511ad7c20f11c5d015068381364bbf06af30a056f`  
		Last Modified: Thu, 04 Dec 2025 20:22:42 GMT  
		Size: 98.5 MB (98542699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52de3bf786c79b5134a0c7b27ca8e0af0c2a3970583e00b78f7b66a4f9ed667`  
		Last Modified: Thu, 04 Dec 2025 20:22:27 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:521e7951443b063f4520089a1ebc6308ecd06aaf1b18c9e98591a5319747f8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48182094f783da762b480d5ced21243438058b63c293dc687da3e35d97b36ac3`

```dockerfile
```

-	Layers:
	-	`sha256:7e0a6a67cf067c1b67105ed97178d0e51129e7e235b4a5f0abd3996ab6927ee6`  
		Last Modified: Thu, 04 Dec 2025 23:52:22 GMT  
		Size: 41.4 KB (41389 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:a579640c57a341f3a58b30592208dcb6e2782cf255c4ab068cdec5a4f9d8ac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279582742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f21159df80ac2116e0e970e190056d67b77064b90c37226ee66ed7d229e801`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 13:00:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 13:00:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 20 Nov 2025 15:05:04 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 15:05:04 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 20 Nov 2025 15:05:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 20 Nov 2025 15:05:04 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 20 Nov 2025 15:05:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 20 Nov 2025 15:05:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 20 Nov 2025 15:05:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 20 Nov 2025 15:05:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 15:05:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 20 Nov 2025 15:05:05 GMT
CMD ["irb"]
# Fri, 21 Nov 2025 09:33:03 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 21 Nov 2025 09:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 09:37:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 21 Nov 2025 09:37:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Nov 2025 09:37:47 GMT
ENV RAILS_ENV=production
# Fri, 21 Nov 2025 09:37:47 GMT
WORKDIR /usr/src/redmine
# Fri, 21 Nov 2025 09:37:47 GMT
ENV HOME=/home/redmine
# Fri, 21 Nov 2025 09:37:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 21 Nov 2025 09:37:47 GMT
ENV REDMINE_VERSION=6.1.0
# Fri, 21 Nov 2025 09:37:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Fri, 21 Nov 2025 09:37:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Fri, 21 Nov 2025 09:37:47 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 21 Nov 2025 09:37:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 21 Nov 2025 10:43:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 21 Nov 2025 10:43:47 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 21 Nov 2025 10:43:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 10:43:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Nov 2025 10:43:47 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 21 Nov 2025 10:43:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb326e4644eb4003f3e3d563fdb529d1bc2c3ba13617e331579c4caa851f628`  
		Last Modified: Thu, 20 Nov 2025 15:06:51 GMT  
		Size: 1.2 MB (1247913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cb328d71adf192ba4d9bc8d47dccdee276e88338e6602f16461a9245b9269a`  
		Last Modified: Thu, 20 Nov 2025 15:06:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81fb1dc3ffb029aef65310d90679ebffdaa9b8791c6566dba3f7e6a17d511b`  
		Last Modified: Thu, 20 Nov 2025 15:06:55 GMT  
		Size: 38.0 MB (37991956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e851e5bd6f0a53627b56c12b4c332ceb761365476f31c7511dec959890280f2`  
		Last Modified: Thu, 20 Nov 2025 15:06:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270b186b0cea7dadc709118d9d910e844ad7de69dfac1dedd773ae7e5cbf5ed`  
		Last Modified: Fri, 21 Nov 2025 10:47:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239781561a8eccd38c69d96f06ecd8aa4e1dc9ce6cede392370015b94ff286f`  
		Last Modified: Fri, 21 Nov 2025 10:47:24 GMT  
		Size: 107.4 MB (107394296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee0e07dbff0671ff328c7b0fe25ef05126e42c7a7586ec8836741758d260ca`  
		Last Modified: Fri, 21 Nov 2025 10:47:18 GMT  
		Size: 896.3 KB (896334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1a2b810df8d065c4c93f955f0032b1e282f33615fb264f536847d0464131b0`  
		Last Modified: Fri, 21 Nov 2025 10:47:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cf547c5675a17194d084b9bbdb648f40c861051dd278a4fe79110935cf0a1f`  
		Last Modified: Fri, 21 Nov 2025 10:47:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a151883bc725c1ebc92e5b0a941a94b83deebf0c92a1ea2be8b5042db281614`  
		Last Modified: Fri, 21 Nov 2025 10:47:18 GMT  
		Size: 4.1 MB (4139981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052e4f68bd3bdd8f2d3b6894751330c22e3f962cc6e5f47ce67a6919a7baeb7a`  
		Last Modified: Fri, 21 Nov 2025 10:47:26 GMT  
		Size: 99.6 MB (99635011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3801789f140941f81022c62ec0877840200631f74b703ff4e231bb8d0fa76e`  
		Last Modified: Fri, 21 Nov 2025 10:47:17 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:530cf6f687784dd176b29204636cee16e40cbf3c7b5849a6aa39d43bd729946e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74babed2bd4c8cc9c29dbfd26a575a96970039ad9f56c9f893b3b4e483b765e`

```dockerfile
```

-	Layers:
	-	`sha256:c576385e1d3fa8cdb3b9a07e1de3048ac27230fc09dd8123626e14958c841fc8`  
		Last Modified: Fri, 21 Nov 2025 11:49:53 GMT  
		Size: 41.3 KB (41321 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-trixie` - linux; s390x

```console
$ docker pull redmine@sha256:d744261d3e96bc3cf4117d98deaa70e72540459110b38c783166408130d2b220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283591428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a0c73d1e31301d5e905ef0289c5d5178a126642fa5d8ff7f7fa2490de533d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

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
# Thu, 04 Dec 2025 20:06:35 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:08:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:09:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:09:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:09:17 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:09:18 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:09:18 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:09:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:09:21 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 04 Dec 2025 20:09:21 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 04 Dec 2025 20:09:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 04 Dec 2025 20:09:21 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:09:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:14:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:14:24 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:14:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:14:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:14:24 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:14:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
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
	-	`sha256:33fa09f7b9996bea74f2c89c676816acbf15a434f31c948bf8c61dcadd0dc3e2`  
		Last Modified: Thu, 04 Dec 2025 20:15:15 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bc4c873a2378c5c317862af69117a26e5e99b4855abf7fed77acb198a70c35`  
		Last Modified: Thu, 04 Dec 2025 20:15:25 GMT  
		Size: 111.0 MB (110950788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5bc25298f6c060a7ab59762fe381c230380bd6c1f9d83a4bfd298dbc38a60`  
		Last Modified: Thu, 04 Dec 2025 20:15:15 GMT  
		Size: 922.9 KB (922879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78de1e118e8e1ea734497f4b541fc2afda74186d68a891eea118ce39857a2b1c`  
		Last Modified: Thu, 04 Dec 2025 20:15:15 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741c1aadabf327da80ebcb70cb975bb59c41de9754eee184c7907bf1ba303ebb`  
		Last Modified: Thu, 04 Dec 2025 20:15:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baac8301400c2d53905d59c146bc0bd6dea8cefdb57ee2a051ba06602f0ba7b0`  
		Last Modified: Thu, 04 Dec 2025 20:15:16 GMT  
		Size: 4.1 MB (4139980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29499f8b083040cfa8759ab2fe7a3365d60d5c625de6120ffafc9a40b992eb4c`  
		Last Modified: Thu, 04 Dec 2025 20:15:23 GMT  
		Size: 97.2 MB (97157848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f22f5912cf6644bcd7f20a78d316e5633b4afac6cf22ef7a9ff71ae2836e74`  
		Last Modified: Thu, 04 Dec 2025 20:15:15 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:cfde3f1f4902e93e21b07ca2dc603e0155dd456f21ba04d20be3a03841ab4db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de8962e471cf4020bb315bf0a0dee4f85e80d3fb78c74e3c38f9fe0dac801d8`

```dockerfile
```

-	Layers:
	-	`sha256:c603a5bc9a84f5aba671b5651efde5758b9c0781c046de484eed516e169d5871`  
		Last Modified: Thu, 04 Dec 2025 23:52:26 GMT  
		Size: 41.3 KB (41312 bytes)  
		MIME: application/vnd.in-toto+json
