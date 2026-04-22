## `redmine:latest`

```console
$ docker pull redmine@sha256:962307b6f3432de53a3381371865a0eeca6845550ecbd1c80ea8391a45a3e621
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
$ docker pull redmine@sha256:865d0cd80296147957b3d06f10d169493713d9e6a6d7b098389d2d678ed7db32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260187556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac6b660cd95ead8cb9863524eea31d355381cc4834b8082c0f19f6f0183c23b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:10:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 02:12:53 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:12:53 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 02:12:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 02:12:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 02:12:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 02:12:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 02:12:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 02:12:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:12:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 02:12:53 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 05:00:33 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:01:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 05:01:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 05:01:04 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 05:01:04 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 05:01:04 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 05:01:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 05:01:05 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 05:01:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 05:01:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 05:01:05 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 05:01:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 05:01:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 05:01:55 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 05:01:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 05:01:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 05:01:55 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 05:01:55 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fb965477c5429b4099ab65962875c6baa9a8f502bea5d946b5d29973009f56`  
		Last Modified: Wed, 22 Apr 2026 02:13:02 GMT  
		Size: 1.3 MB (1279835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b04a9376a494d0c0df5d19bac489deb83e2af58a4e18c69cd9bd2d29f47126`  
		Last Modified: Wed, 22 Apr 2026 02:13:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e22d71033b81b50f4b9304de633a51b69d43d08db71cac6c9466c18293659aa`  
		Last Modified: Wed, 22 Apr 2026 02:13:03 GMT  
		Size: 42.1 MB (42127230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f142f4c1a780bfa2a017a1937711d76ccac1615dea3b45b76d64ba614ea8e41`  
		Last Modified: Wed, 22 Apr 2026 02:13:02 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393be1a3e872891641462adebc3033815dabb460c8f90f2f63c167a898fb0fe5`  
		Last Modified: Wed, 22 Apr 2026 05:02:09 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef903e5ee3f9afba5ce39b7016e3aabb0d426df0e271f1f7aae05e054b729`  
		Last Modified: Wed, 22 Apr 2026 05:02:11 GMT  
		Size: 110.1 MB (110144838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa07bad4bee76eeb51616f747ed875c54f13474d570ae8fffff253cfede8e52`  
		Last Modified: Wed, 22 Apr 2026 05:02:09 GMT  
		Size: 950.0 KB (950043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e05b6165647a18724fa58e23d31f6b213d5aab14a53c80b8d6d03176fa5256`  
		Last Modified: Wed, 22 Apr 2026 05:02:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678293c56efe71ba483a1e662a305b4a63fe6fd8372b89e585b3b6b782be3945`  
		Last Modified: Wed, 22 Apr 2026 05:02:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a4456d13ba6f7aaca66a1d5d6b3d99ab66d21e725c05c266d8985e4e7786d`  
		Last Modified: Wed, 22 Apr 2026 05:02:11 GMT  
		Size: 4.1 MB (4149080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c118249d69ce06f2c7a67ebf757508238a1d8b6919f772b7b2cff186db44757`  
		Last Modified: Wed, 22 Apr 2026 05:02:12 GMT  
		Size: 71.8 MB (71752245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3096aaec2e1a30a3c1177ab6b98494d974ef307831e5a2dbb3fc5bcc57cfc490`  
		Last Modified: Wed, 22 Apr 2026 05:02:11 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:4c4f3588df54e85a25de71921c40273c6e2fe4f2b9a4301b148c2fd4ce751d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286d75cc7e1b0828a421743369cb3bc90c3f7f10b94cb4d31cc12b60fe6a31a0`

```dockerfile
```

-	Layers:
	-	`sha256:91e707416b4ca719a092e7d3dcebffe64929c422f4b8387f632bf63346c4d6ee`  
		Last Modified: Wed, 22 Apr 2026 05:02:08 GMT  
		Size: 41.3 KB (41311 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:42e4949989633c0606ebc710023601f945ded1b084a0adc2593019344abc5657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265893009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a97aa3f8a2c1c8b9cf3df4ff1dc41dde41e026afb3b3e212c6b07dd0bad383`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:57:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 03:00:29 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:00:29 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 03:00:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 03:00:29 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 03:00:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 03:00:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 03:00:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:00:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 03:00:29 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 04:09:18 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 04:09:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:10:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 04:10:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 04:10:09 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 04:10:09 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 04:10:09 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 04:10:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 04:10:09 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 04:10:09 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 04:10:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 04:10:09 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 04:10:12 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 04:11:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 04:11:44 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 04:11:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 04:11:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 04:11:44 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 04:11:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb6a935935cfbbc8b471cc038313627c8bcb50e8a6a276b4cbd5674abdfc02`  
		Last Modified: Wed, 22 Apr 2026 03:00:41 GMT  
		Size: 1.3 MB (1263606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a54570e91d1e3a9a1b6a909ca6dbfe80863f5f1873687a3da56c95fc5081f2`  
		Last Modified: Wed, 22 Apr 2026 03:00:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fcc5c941806aef15b227dbda51f0e863c309f400001fe773e1f1e87bedb336`  
		Last Modified: Wed, 22 Apr 2026 03:00:40 GMT  
		Size: 37.9 MB (37924118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d79b9e57677046ca478dbfa398fc7f0a476da55a068b7acf417fd739e833b`  
		Last Modified: Wed, 22 Apr 2026 03:00:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d220bc763145a44c8b85884433012d12ad04050780c4b6990db4b6ddc14fe113`  
		Last Modified: Wed, 22 Apr 2026 04:12:00 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731adc2dd4122b9a8a97009f8d0f1a7dd33c1a9c1af0d74431b2fedb51eabef`  
		Last Modified: Wed, 22 Apr 2026 04:12:04 GMT  
		Size: 105.9 MB (105938948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01643a0f249928f654afcfcd3cebda5a7a8942e9e9d023e64fe72a43534946a`  
		Last Modified: Wed, 22 Apr 2026 04:12:00 GMT  
		Size: 919.6 KB (919560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25955d0a6e9873529486d131ca66d52625f6d325b8dae0102575f61aa8ca87df`  
		Last Modified: Wed, 22 Apr 2026 04:11:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dbee851bcc65a4da7495b168d3a10d62d11f55fcffda98df6de9de190d590d`  
		Last Modified: Wed, 22 Apr 2026 04:11:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ab21955c1b342b291a2071b2325166d91ea8d7c7e79f29c3046d81e5947808`  
		Last Modified: Wed, 22 Apr 2026 04:12:01 GMT  
		Size: 4.1 MB (4149080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4711a9fad9a6b8f4e475130b530087d2b033c174935d748c1c1cfd28f3abaf11`  
		Last Modified: Wed, 22 Apr 2026 04:12:04 GMT  
		Size: 87.7 MB (87745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c658aba131bec6d8846d76a118e958453ec14244a560c7af76ddb6b9e39c0fcc`  
		Last Modified: Wed, 22 Apr 2026 04:12:02 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:8da21a30bb68b85939d9d305ba633f70d13ac52cc0714bce6b00dc1013c4d027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718c1e440ce38194f5d3e008bbc14256945d2cd08a8b37d79526bfb196cddef9`

```dockerfile
```

-	Layers:
	-	`sha256:e00ea012357922298f4305badc178822181bb4500aad207e2ab955120f79bdf8`  
		Last Modified: Wed, 22 Apr 2026 04:12:00 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:f919b2abd6503d083ea7225497338ed9a022c2f1fdaafdac9ef319d43725bbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258694737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994de065b4d222e338b9ede5dc60757d1dc9efd07857bd70cdc38b7d989cc901`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:27:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:27:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 03:30:40 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:30:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 03:30:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 03:30:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 03:30:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 03:30:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 03:30:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 03:30:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:30:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 03:30:40 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 04:20:15 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 04:21:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:21:27 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 04:21:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 04:21:27 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 04:21:27 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 04:21:27 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 04:21:27 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 04:21:27 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 04:21:27 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 04:21:27 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 04:21:27 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 04:21:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 04:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 04:22:52 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 04:22:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 04:22:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 04:22:52 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 04:22:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592654af5f11d5b3e869f48d90905a3a49273037e3e24dacc6e94a8541881fe6`  
		Last Modified: Wed, 22 Apr 2026 03:30:49 GMT  
		Size: 1.2 MB (1237490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f067b523d857589d67ab4f2f604a02dcdc1164264f0bb9a9aa115cfee4059d6`  
		Last Modified: Wed, 22 Apr 2026 03:30:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431f1ab330c6bb3b39bbbc33ccf90ac0f65547772e28762708d45478571cb1a5`  
		Last Modified: Wed, 22 Apr 2026 03:30:50 GMT  
		Size: 37.8 MB (37780656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b63779522082e8ba1e6f88945694f5205a6505b3881d1018d9c4e07259acbd`  
		Last Modified: Wed, 22 Apr 2026 03:30:49 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89250b4b62ceebaff7954c5e1162437aed95c7d7e0ad5e49e695a7288dc02895`  
		Last Modified: Wed, 22 Apr 2026 04:23:06 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ae6a82da8a23baee152fbad4197152b82abae61e68632fd3f7c3fdf3d436c5`  
		Last Modified: Wed, 22 Apr 2026 04:23:08 GMT  
		Size: 100.8 MB (100825470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836b18a98953e4a045f93aa40b6e7136400088217227e68d6cbfcd5895796bf1`  
		Last Modified: Wed, 22 Apr 2026 04:23:06 GMT  
		Size: 915.5 KB (915523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefa44a4cdfdd2cdaabb81a55ded4d787f72ed5df43ed6bfdd4f7ee736b0ed3`  
		Last Modified: Wed, 22 Apr 2026 04:23:06 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cff4c32718d06f97c9f3667372e7a2f6676559e6baaf828c606e6c7d02593b`  
		Last Modified: Wed, 22 Apr 2026 04:23:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cee81c224bd32cd608f13c830e939a07036ef4ed2aaf8e7526bec53f425da8`  
		Last Modified: Wed, 22 Apr 2026 04:23:07 GMT  
		Size: 4.1 MB (4149089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f885ea1015ae3ca6016493123801b026f3836226257a3e8a1cd2bcbeb68e83`  
		Last Modified: Wed, 22 Apr 2026 04:23:10 GMT  
		Size: 87.6 MB (87567559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942c700bfaa699c13c94e27d97122c3999bedf7d2fb5f7a64fda5d808b97b76b`  
		Last Modified: Wed, 22 Apr 2026 04:23:08 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:94e35c0b7655c0a4d42c3217f4275df7ab9873ee90852eddfcf9f12a98368107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac950bc4324ff3cde894d1007ddb41df86cfb591b3fa8cbb772d47289a8668f1`

```dockerfile
```

-	Layers:
	-	`sha256:05d3b989abfdc47f4488f260d0c3d125d6b419a4f7443b21d6444a06650a94e6`  
		Last Modified: Wed, 22 Apr 2026 04:23:06 GMT  
		Size: 41.5 KB (41488 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:6cab5c5464e4c7c522c1f412ed00c56c7bda270960944844a98d94e1cbc90409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258669506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8656dbc60c32ec81dcc78725322e1f2d90339a3bddb380508b4f8f1dd7701d21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:15:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 02:17:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:17:56 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 02:17:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 02:17:56 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 02:17:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 02:17:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 02:17:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 02:17:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 02:17:56 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 03:23:51 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 03:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:24:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 03:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 03:24:28 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 03:24:28 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 03:24:28 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 03:24:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 03:24:28 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 03:24:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 03:24:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 03:24:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 03:24:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 03:25:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 03:25:31 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 03:25:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 03:25:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:25:31 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 03:25:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d8ae85f1c668c76c20cb628aed41dcf5a2d3cb62225cfb63bf7d8ae99cd819`  
		Last Modified: Wed, 22 Apr 2026 02:18:06 GMT  
		Size: 1.3 MB (1261698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3f3a6f1b816732de46704b9e6307fa13e15e080fc4ffc65e1071e121327680`  
		Last Modified: Wed, 22 Apr 2026 02:18:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5165ce01ff14401c54877c3d8176a63b6199bf771fd2be69df7d8458e320d7`  
		Last Modified: Wed, 22 Apr 2026 02:18:07 GMT  
		Size: 42.1 MB (42078861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6bb1267f65291449358ab9beff68a54c151ba1fbc0aaa69ef97603b89b1895`  
		Last Modified: Wed, 22 Apr 2026 02:18:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5bbae1f2e93ec46b52bd16d83aca724e495b101d5e4d2fbe069b1336ab947a`  
		Last Modified: Wed, 22 Apr 2026 03:25:46 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c748be8b2bc15ad434b328f109135b41945abfbe303877a2b308d6d55170e`  
		Last Modified: Wed, 22 Apr 2026 03:25:49 GMT  
		Size: 108.6 MB (108562511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4396119d0de87c77c381df45040b478e26adf276b2e60d299ff82d0bba69aa`  
		Last Modified: Wed, 22 Apr 2026 03:25:46 GMT  
		Size: 903.4 KB (903398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5deda82d8b08ce9bc59ef6d67624dceeafdd79a178d9b4d011ebb1f0e71b3c8`  
		Last Modified: Wed, 22 Apr 2026 03:25:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4aceea98f3a5abe9f9bea8582dda7aa2bda6b86c163a9323e842d7a136c15c`  
		Last Modified: Wed, 22 Apr 2026 03:25:47 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7a9abc3790491e08335dc4b132e9ed07aacd424ca434cb5bf294a1d05bab5f`  
		Last Modified: Wed, 22 Apr 2026 03:25:47 GMT  
		Size: 4.1 MB (4149088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2769d0912fb807d4dfe4d4b06227d81451d1bf2ed43c4a4460520a559b9cb490`  
		Last Modified: Wed, 22 Apr 2026 03:25:50 GMT  
		Size: 71.6 MB (71566228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d5d2e18df5ac5288f3eb17a36154a58d62738fdfcc6f87a63e9ee1748a1d5`  
		Last Modified: Wed, 22 Apr 2026 03:25:48 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:0281e80029d19342c2ec6a95948226cf3afb9b737aed0c788f7f178dd1d509c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8396a2e2fec2828332cff29e4ffc56dd967171c1be7a3a7a1bc48d710a84e54`

```dockerfile
```

-	Layers:
	-	`sha256:94b2893a34a3f9c86f9af6672c0024b9b7d25af8668dddc78275461e970f33ee`  
		Last Modified: Wed, 22 Apr 2026 03:25:46 GMT  
		Size: 41.5 KB (41539 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:44502f48f063c920de984afef0757b9501276e13b44765a32d4ec0f12641556d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278022072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e83a50b300db38b09d6cda3c0da595059fb8bd51f4bdc2065a9c892c82a61c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:17:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 02:20:21 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:20:21 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 02:20:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 02:20:21 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 02:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 02:20:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 02:20:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 02:20:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 02:20:21 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 05:17:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 05:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:17:41 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 05:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 05:17:41 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 05:17:41 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 05:17:41 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 05:17:41 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 05:17:41 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 05:17:41 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 05:17:41 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 05:17:41 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 05:17:43 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 05:19:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 05:19:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 05:19:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 05:19:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 05:19:02 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 05:19:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daee4f308978661c4f701ab0b42b4bc31d3b084eddd8745e7f5e30f2e95386af`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 1.3 MB (1287464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ebad5e13da040b0c72109d4a7eab512f380851dc46a9ab6230cc58bbdd9bab`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147e32f676b942b4494dda1fb0a38f3b7712c788737b89660affa8498b46ccad`  
		Last Modified: Wed, 22 Apr 2026 02:20:30 GMT  
		Size: 37.7 MB (37661685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d137e5bcf76819216f805740093f404f928c61e36d351fa088a5fac2455c42`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dc966892071aee54c7673af7ce46291a86f71701de96f771b9ead70879f06c`  
		Last Modified: Wed, 22 Apr 2026 05:19:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14093735b3e86c54b94572693613d1e5ff52560b567659c4ee11be25678e10d`  
		Last Modified: Wed, 22 Apr 2026 05:19:19 GMT  
		Size: 112.7 MB (112669686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dbefdef001c0379b977ef83e126d1e3342f4cf05ef4b8c2fbb683a577963b5`  
		Last Modified: Wed, 22 Apr 2026 05:19:16 GMT  
		Size: 918.8 KB (918818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f972ef27979879dbd4eff0741462bb1f548ef47a8661bbd0240b35cf4c8b9e`  
		Last Modified: Wed, 22 Apr 2026 05:19:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a38e751f88452cb25f99abe7b586d54f5617c46f789bbddf77738334e1688`  
		Last Modified: Wed, 22 Apr 2026 05:19:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc2c943106f203de155977ca3f93b6b791edaabf399ab6f3db16e3d369b52d`  
		Last Modified: Wed, 22 Apr 2026 05:19:17 GMT  
		Size: 4.1 MB (4149087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade2570d5cb4222b80b21dc8c992b061c9a24679e17969cb9088a059b0efb9e2`  
		Last Modified: Wed, 22 Apr 2026 05:19:20 GMT  
		Size: 90.0 MB (90034888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ba527391bd64c2705f67761380a2614698c6f9cbd8e1312f76102d84af52b`  
		Last Modified: Wed, 22 Apr 2026 05:19:18 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:f6548e2e43dceae82ffd9a5cc41d7b2554fb364d8d855d7e4244af2513ab6a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239fa1baeda2173d7f5b78486d943fa0bd332f63bcb9de8e3b118c3bba119d0d`

```dockerfile
```

-	Layers:
	-	`sha256:f05db1ed58076be52c27895da00636c1e041b09779241644d7271bffcd06f663`  
		Last Modified: Wed, 22 Apr 2026 05:19:16 GMT  
		Size: 41.2 KB (41249 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:214f898ff96b9db5748c9d3f88db9749491e5bf3149708a2219270bd1923680f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301808065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2a92b240d22dc856904dae9bf67e1d2cac871aab44368d4da0479dd543210`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 07:49:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 07:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 08:04:05 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:04:05 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 08:04:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 08:04:05 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 08:04:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 08:04:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 08:04:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 08:04:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:04:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 08:04:05 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 12:00:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 12:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 12:02:35 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 12:02:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 12:02:35 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 12:02:35 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 12:02:35 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 12:02:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 12:02:36 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 12:02:36 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 12:02:36 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 12:02:36 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 12:02:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 12:07:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 12:07:18 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 12:07:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 12:07:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 12:07:19 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 12:07:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881af0366cada83b9c9ab9337fb1fd45d3e9e2c7ff77a7a84945892ac2afa03a`  
		Last Modified: Wed, 22 Apr 2026 07:54:54 GMT  
		Size: 1.3 MB (1309849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa30345138687d868453f6b413d1c6981e7057b7aaa19c55dc9099e48fd6a6`  
		Last Modified: Wed, 22 Apr 2026 07:54:54 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa5c6f57a9d9cfefa785bcd2f772b441e730430294859a59c3c8e832ebfdac`  
		Last Modified: Wed, 22 Apr 2026 08:04:28 GMT  
		Size: 39.5 MB (39532194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b87cadc542a3eaf171b4b042486a4b5ebe818dab787fd396f84a07a0e12d7`  
		Last Modified: Wed, 22 Apr 2026 08:04:27 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb8ce68b8839221b0bfeb361b21e7c466c9537dd4c5fdeb06d1a40908f080e`  
		Last Modified: Wed, 22 Apr 2026 12:07:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa40f6e9cf2f398f8df9c003c629f586c967fd8c9bbfc2a9b7fb4b68f2e5c8`  
		Last Modified: Wed, 22 Apr 2026 12:07:57 GMT  
		Size: 117.6 MB (117632459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf80f2b5bf9328b7e2642b7dc950f6cc84fbf65723f35b738deb35e58fa1c06`  
		Last Modified: Wed, 22 Apr 2026 12:07:53 GMT  
		Size: 909.4 KB (909419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6a0b0e708a6e9a1a4cf7b953c193134d831281a6c8549c6dc18080a448a49c`  
		Last Modified: Wed, 22 Apr 2026 12:07:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f557d28eed356c5779f959a2f3e3cafb07638d2281667ce59d5e59305cd87cc`  
		Last Modified: Wed, 22 Apr 2026 12:07:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471b0d2977da338976c5f72be98d3bb7817b6e8d64f6d7fa8130b29d369dd0f5`  
		Last Modified: Wed, 22 Apr 2026 12:07:55 GMT  
		Size: 4.1 MB (4149083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f4b5829c06efbd832d2eb5b6ae32a9c3613be04c4db2f95b54e31749407d0e`  
		Last Modified: Wed, 22 Apr 2026 12:07:59 GMT  
		Size: 104.7 MB (104672913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f66c3336ec5c0dfec2b666be79042022df9b1b0fa8dd7c99cc2442b836f8f7`  
		Last Modified: Wed, 22 Apr 2026 12:07:56 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:4b67c366fbec338a9d5a7e60e065f9966692eb3837e4bcabe5414f41e60c6e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e829421feb12b13f1a7aea4f49ada0c1e597d1dd74c7c63a0e88915a97de5e22`

```dockerfile
```

-	Layers:
	-	`sha256:24054b26107cb306d9cdb5390a1d5040bdcc96f6f59a3656af4a3529855b961b`  
		Last Modified: Wed, 22 Apr 2026 12:07:53 GMT  
		Size: 41.4 KB (41392 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; riscv64

```console
$ docker pull redmine@sha256:a6d0d6422d63358a11fffb5475ff3f33259a3443ec5773975d71dd0e4a5ccc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287905749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f89f116cebd7b719bbda30f1ff7c8c918d0825fde3e56359d14a0e22f3146e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 19:58:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 19:58:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 10 Apr 2026 00:06:03 GMT
ENV LANG=C.UTF-8
# Fri, 10 Apr 2026 00:06:03 GMT
ENV RUBY_VERSION=3.4.9
# Fri, 10 Apr 2026 00:06:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Fri, 10 Apr 2026 00:06:03 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Fri, 10 Apr 2026 00:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 10 Apr 2026 00:06:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 10 Apr 2026 00:06:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 10 Apr 2026 00:06:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:06:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 10 Apr 2026 00:06:04 GMT
CMD ["irb"]
# Sat, 11 Apr 2026 23:27:50 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sat, 11 Apr 2026 23:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Apr 2026 23:32:42 GMT
ENV GOSU_VERSION=1.19
# Sat, 11 Apr 2026 23:32:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 11 Apr 2026 23:32:42 GMT
ENV RAILS_ENV=production
# Sat, 11 Apr 2026 23:32:43 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Apr 2026 23:32:43 GMT
ENV HOME=/home/redmine
# Sat, 11 Apr 2026 23:32:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 11 Apr 2026 23:32:43 GMT
ENV REDMINE_VERSION=6.1.2
# Sat, 11 Apr 2026 23:32:43 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Sat, 11 Apr 2026 23:32:43 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Sat, 11 Apr 2026 23:32:43 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 11 Apr 2026 23:32:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 12 Apr 2026 00:42:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 12 Apr 2026 00:42:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 12 Apr 2026 00:42:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 12 Apr 2026 00:42:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 12 Apr 2026 00:42:25 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 12 Apr 2026 00:42:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a665d7345a4e5149ccc3bc1507f501519344c2cb6c1782b05128202868cdc25e`  
		Last Modified: Thu, 09 Apr 2026 22:01:49 GMT  
		Size: 3.9 MB (3869420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e93ccf45d0f580da9a1544ac8698216ba855f5724ad6ed077c06d3d7b8751`  
		Last Modified: Thu, 09 Apr 2026 22:01:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e85773cd15f68f9572df4484bd1d6e8b5166b9109d8a2af2de9254fa39e8c`  
		Last Modified: Fri, 10 Apr 2026 00:07:43 GMT  
		Size: 38.0 MB (37972763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd789a08630f7c9c2710e11fe129c3cb142d7f5b05b15f20a4a4af32cb4dd69`  
		Last Modified: Fri, 10 Apr 2026 00:07:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e41f04d9aa2bf224e51546d308b15be5d7538988eb29c56a8a316fdd06f57a`  
		Last Modified: Sun, 12 Apr 2026 00:45:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383df23ed79d3aa0e107d88b37b507c5ed803fb679da66263040f18883f8ec8`  
		Last Modified: Sun, 12 Apr 2026 00:45:48 GMT  
		Size: 107.4 MB (107417324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc72ddf5939ca2c7b0575ec434e9bb194f3e7a9783e6a9c5bdee53fbb3009bb`  
		Last Modified: Sun, 12 Apr 2026 00:45:18 GMT  
		Size: 896.8 KB (896835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48ebe595a55bdb450615f07cea9a9fcf073671efe223c69acaa6714bd0da5b`  
		Last Modified: Sun, 12 Apr 2026 00:45:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa5f72e15db798fbc25041d8d1419132c3eb18b0bd9aa93aa189b404b304963`  
		Last Modified: Sun, 12 Apr 2026 00:45:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8518d71674c2638d91759b24cdc216c71d11a4a7ad84f733f3acd896f1274fef`  
		Last Modified: Sun, 12 Apr 2026 00:45:22 GMT  
		Size: 4.1 MB (4149087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8887defe2b590b7aa480917674bda6b765efa6ba7ec019ff3d7bf9b7a6f0694a`  
		Last Modified: Sun, 12 Apr 2026 00:45:49 GMT  
		Size: 105.3 MB (105320423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f410747ecf48592778dd5fed3e8105ced751246bc85e7cb48c3b47c47022355f`  
		Last Modified: Sun, 12 Apr 2026 00:45:22 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:7cf5ec1094e589a17917811891258aed269a8b6f96fc90c6e2132abadee36c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c44bb7ed611b25b6490d76e75e0be3039742d48a584ed108ab092808f1458f`

```dockerfile
```

-	Layers:
	-	`sha256:bd8b0423490c09e76beda70dac7510cba1278df433f166615b27d3787a61072f`  
		Last Modified: Sun, 12 Apr 2026 00:45:18 GMT  
		Size: 41.4 KB (41392 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:4cbc2edb842c5cc8c319b00e83e9790f4a1933cc4a811cf8dc61666285dad10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289630243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ba81c60768cbd6ec14088f17e6ccde73c3b2294459c71320a57d0c06744b68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:47:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:48:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 03:54:12 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:54:12 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 22 Apr 2026 03:54:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 22 Apr 2026 03:54:12 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 22 Apr 2026 03:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 03:54:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 03:54:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 03:54:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:54:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 03:54:12 GMT
CMD ["irb"]
# Wed, 22 Apr 2026 05:01:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 22 Apr 2026 05:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 05:02:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 05:02:33 GMT
ENV RAILS_ENV=production
# Wed, 22 Apr 2026 05:02:33 GMT
WORKDIR /usr/src/redmine
# Wed, 22 Apr 2026 05:02:33 GMT
ENV HOME=/home/redmine
# Wed, 22 Apr 2026 05:02:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 22 Apr 2026 05:02:34 GMT
ENV REDMINE_VERSION=6.1.2
# Wed, 22 Apr 2026 05:02:34 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Wed, 22 Apr 2026 05:02:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Wed, 22 Apr 2026 05:02:34 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 22 Apr 2026 05:02:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 22 Apr 2026 05:05:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 05:05:31 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 22 Apr 2026 05:05:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 05:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 05:05:31 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 22 Apr 2026 05:05:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a71821f9d84c9b2271b39af3899553a747f2440319089ef472493d6d5d1dcf`  
		Last Modified: Wed, 22 Apr 2026 03:51:02 GMT  
		Size: 1.3 MB (1294690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b7cb283ca12da051fa2ba74c7703f8d5167ac928a9e03d8a8825ec0950101`  
		Last Modified: Wed, 22 Apr 2026 03:51:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538cc6675985bed48e84875c06cd4e86c9e0d3738cfa5ad4e114378ad073d170`  
		Last Modified: Wed, 22 Apr 2026 03:54:27 GMT  
		Size: 39.2 MB (39206396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fc9f6b2463657ef48bf9c8a6b544b1b884bb4ab80619fec4b2965c6a9970c5`  
		Last Modified: Wed, 22 Apr 2026 03:54:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd7e52800990d5645e776000c0f50ebc12adae22f5a95970a93130e00a74601`  
		Last Modified: Wed, 22 Apr 2026 05:05:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80b02f079055772f4b68a4af668e51852351e36f91ff74674130f8fcda70af`  
		Last Modified: Wed, 22 Apr 2026 05:05:56 GMT  
		Size: 111.0 MB (110981390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86c154cc9e2f52d560dee568c84acf03e5312875add48636b9236dcca2add85`  
		Last Modified: Wed, 22 Apr 2026 05:05:54 GMT  
		Size: 922.5 KB (922516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5accac4c985af48758d98f84c7d6fbb7ef6107976575d71e1216fdfb0c598182`  
		Last Modified: Wed, 22 Apr 2026 05:05:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516aa4e9d5a413970c43cbee81b43919e13a535d5ae1bfb437e7e1543fa4c9aa`  
		Last Modified: Wed, 22 Apr 2026 05:05:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f893cf72d03a2d67b9f13c3a803bdfea13bf667d12e4635a6379692561c40327`  
		Last Modified: Wed, 22 Apr 2026 05:05:55 GMT  
		Size: 4.1 MB (4149086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7b0bbc6327d2e36cf9c2754418b8e9b3e98c751ce7e4eeefd190bbc1e1aab2`  
		Last Modified: Wed, 22 Apr 2026 05:05:58 GMT  
		Size: 103.2 MB (103231749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1e99f9e8c607823b5cd3f3f8a9988df3f6c0153cd7540e50017ab4ee96ec19`  
		Last Modified: Wed, 22 Apr 2026 05:05:56 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:529dfe6ab781a3c755b002db15f0034590e0474818c147b5a174b936ef9c4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e40b3237f494f8f544c7aeed87c6c51e8db46911e830f8578b9e277d240d62`

```dockerfile
```

-	Layers:
	-	`sha256:fc1d1ad01a5f70520a96716e2e260614c9f6420007ef02b276af0e1bbc70fc6a`  
		Last Modified: Wed, 22 Apr 2026 05:05:54 GMT  
		Size: 41.3 KB (41314 bytes)  
		MIME: application/vnd.in-toto+json
