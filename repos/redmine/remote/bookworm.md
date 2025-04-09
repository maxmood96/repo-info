## `redmine:bookworm`

```console
$ docker pull redmine@sha256:2d75fafd16636bf718f095b8c8f79ac6ef668871d6ac63acb6b0684e3447573b
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:99b3a0c3e3e970e8e8c4dd9d1f4dfd6c5fc740eea87deef61c4ad4242c04a545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254763741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6122d9ed6428f8f63e193a8aac7505c684c7ce73e04682bcb1351612ca2b2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 11 Mar 2025 02:53:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3280fae10b5fdc806aadb0936e2e2ff2a5d3dd0033922aa7c8aaeda81f7c`  
		Last Modified: Wed, 09 Apr 2025 18:33:48 GMT  
		Size: 3.5 MB (3499323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233a3ba8f07768620ffa7ed8bd6eb8ebb7fe518ec429f75a01518eef96b6dd0c`  
		Last Modified: Wed, 09 Apr 2025 18:33:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46caff58e6d976e5acb55c6f4e054aa8e2deedb9bc849bca484245cf2c9b9e31`  
		Last Modified: Wed, 09 Apr 2025 18:33:49 GMT  
		Size: 37.7 MB (37740889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d510fe2bd53875865814ff5dd8b7c4ce7ba6d951ce6ec36f057975ceb73248`  
		Last Modified: Wed, 09 Apr 2025 18:33:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc3d92a786dca31cca4ff525794817876c35d53daac5c1bdedc329173dede8c`  
		Last Modified: Wed, 09 Apr 2025 19:05:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585cde20dc77140b9cd0001238b13bb4f427fb690a52c7640ea61d54f1ebeebc`  
		Last Modified: Wed, 09 Apr 2025 19:05:47 GMT  
		Size: 123.1 MB (123122027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963bcc96f953e4d794cafdc5c1017d6b227d621c7dc87df6191814d387c542ea`  
		Last Modified: Wed, 09 Apr 2025 19:05:45 GMT  
		Size: 1.1 MB (1143527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd28b772ea18c429dec6c8fa612d8c738c78225d9a0e070b1f6a0a62f6a4cb6a`  
		Last Modified: Wed, 09 Apr 2025 19:05:45 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c34d2a7e8a1ee636491032e74388227e804ef397934a746450c1677771cc26`  
		Last Modified: Wed, 09 Apr 2025 19:05:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f519d55383587127e63db0ea08c0887683123417d4d5b134bb38a5f7df2b38`  
		Last Modified: Wed, 09 Apr 2025 19:05:46 GMT  
		Size: 4.1 MB (4056919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb300a00a30295cc9ed1ecd7d05aec5e62d9a7b7c87050eadaef1cf47279b51`  
		Last Modified: Wed, 09 Apr 2025 19:05:47 GMT  
		Size: 57.0 MB (56969787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdd2e734e873064aafadf948a44962b2b3641523f89e4152caf502563794e4`  
		Last Modified: Wed, 09 Apr 2025 19:05:46 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:151e5402b81d34c3a6fd45931e2ab26e4393e93fe1a8ddd51c8f9c057a100dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfa70679ede778e63512fe63c6fd34ddfd2a748c3564d11636c59ff178ee0ab`

```dockerfile
```

-	Layers:
	-	`sha256:2ea4ec7b330bb2931615fc29c5a37e8d60292f8d2a4c757239065287164d8004`  
		Last Modified: Wed, 09 Apr 2025 19:05:45 GMT  
		Size: 41.2 KB (41250 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:0e5eab77edb49870c9142251dd7285bfcb161d274a7eff3f03ed848c2b1b4b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239189093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf355d8dc32d86743b4dc436187279189377fe2aebbf811d22497818d6fdae7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 11 Mar 2025 02:53:30 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91528d2a0bc959da97069f85dfc6ccf3eebbe0bf54474fb8ac945096ae8ed3cc`  
		Last Modified: Wed, 09 Apr 2025 19:35:20 GMT  
		Size: 34.3 MB (34288802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dfc1b45c5d7b9d1e1d21b644f5a134ffb0e4bb784e3a4e54156540f7c75c31`  
		Last Modified: Wed, 09 Apr 2025 19:35:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba27b255f8ad8cf73e9ede86126ed50f67812895a38ae035c3d228ad0be1b09`  
		Last Modified: Wed, 09 Apr 2025 20:10:45 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6502e0da79a66c0b00cfce655321dad10f434fdd99c9f2f9d798749810299a`  
		Last Modified: Wed, 09 Apr 2025 20:10:48 GMT  
		Size: 116.8 MB (116762264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0d12ddea50443be25ab79e409ce61105934d789af26da475c2e0e3389c6ae`  
		Last Modified: Wed, 09 Apr 2025 20:10:45 GMT  
		Size: 1.1 MB (1120886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f57b9db159dbd1e5674d982d3309d69c1010de5c5b1d0479d7450c0c70b152`  
		Last Modified: Wed, 09 Apr 2025 20:10:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660aeb4939a8437be08897bb75a09ab0a3e7d62f5aab9cfc12974ea64d867aae`  
		Last Modified: Wed, 09 Apr 2025 20:10:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe9a7fe9fc740ae108219f44159522d2ae2b46e3f475b9082a6ca9bd396f6e1`  
		Last Modified: Wed, 09 Apr 2025 20:10:46 GMT  
		Size: 4.1 MB (4056916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b419939faa6e104e80d8a914ce8930aecd207f37b0a9df95eb1cfff39023b3`  
		Last Modified: Wed, 09 Apr 2025 20:10:48 GMT  
		Size: 54.1 MB (54124939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5689f9979ea3a94f01a934dfdd84221288888d729c5ef97f7e6eb30d799d72`  
		Last Modified: Tue, 08 Apr 2025 10:32:13 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:2e51cbaa121b9ba6d1ef26ea78e9b40859457945223db4983176d015f82dc3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc4551d32360740ba0b8fcda849777782f49e673e5c5dc4dec8c3f47125faa`

```dockerfile
```

-	Layers:
	-	`sha256:80a1323ff6239d9f2658031738fd87ba1aeed8506bf1aac583850d06bd69eac4`  
		Last Modified: Wed, 09 Apr 2025 20:10:44 GMT  
		Size: 41.4 KB (41424 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0a56ab16a063533bd7cb135befc57d33a643da24d5a8bf2b1cc280ee71ec8e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232532384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e1be9c983dab463d2370c6a51905eacb250bebf18e33d06bc0eda5c1f555c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc9f24d0120921823e4d02f5f6ddc1b7b360f3f5b5d431aaf6a859f439d9b7c`  
		Last Modified: Tue, 08 Apr 2025 16:32:56 GMT  
		Size: 34.1 MB (34126649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03707ecced234d137f976b644506cbb6304d79d8019b9d13333919d62e8a712e`  
		Last Modified: Tue, 08 Apr 2025 16:32:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb7a8460de846fd98513c56c65a2d30f9112a8018f146031d101aefeec4cef`  
		Last Modified: Tue, 08 Apr 2025 21:22:49 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5caece0ca9151a3322958e97025ebb7b219869c56a7367987cbcb2091810067`  
		Last Modified: Tue, 08 Apr 2025 21:22:53 GMT  
		Size: 112.1 MB (112140448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe0b527456a3253fb6f97f2fa8f865aad6a73fadd69f0bac785e116ca2e13c`  
		Last Modified: Tue, 08 Apr 2025 21:22:50 GMT  
		Size: 1.1 MB (1110098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29b8ccdc1621c6168e71fbe9edf7a4913b2c451e60fcbad8b1649d2637df118`  
		Last Modified: Tue, 08 Apr 2025 21:22:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0393946a9029830f2c7b992b01cc77391eabb16acb1e1106f6b70c08743daab`  
		Last Modified: Tue, 08 Apr 2025 21:22:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631b27cef56c96b3acb4f74ac353ba48dbe697144d9b7da42f36011dc34d9fa`  
		Last Modified: Tue, 08 Apr 2025 21:22:51 GMT  
		Size: 4.1 MB (4056913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251df160f412a5de1173810525168cb2822027c7be6b101ca0bc9f7d9476800`  
		Last Modified: Tue, 08 Apr 2025 21:22:52 GMT  
		Size: 54.2 MB (54248622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3190ddd940c18185c7895a7150c7457ddb0c855cda6c0fc5dec0433472f86574`  
		Last Modified: Tue, 08 Apr 2025 21:22:51 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:700dd8a22aff749706eb84a301b1a664a4c208a9c62e4d3cb6676a10f54e5ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d709b899284ec5c1ea9e77100e57d0e3e9fff0f9f537e2e3308b60d2d2c372c`

```dockerfile
```

-	Layers:
	-	`sha256:692ba7af96220c08e08de00eb6983fc9e3e9a32448bd10f019b4713abaf35473`  
		Last Modified: Tue, 08 Apr 2025 21:22:49 GMT  
		Size: 41.4 KB (41425 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:d0d6f27f176c087e299656b510baf78de80c1d5262c97734aac082845628b142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251242781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb745f99e38bbae6f362eee889f7087b9a80826069938ce59de8570db163e2cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fae63766ccb69dffa8068bda9cb7df860809ee1cdd67996784e28875b1ec0c`  
		Last Modified: Tue, 08 Apr 2025 10:33:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfe51dc869df5aad796c3ae06fdba321f557b2c6f07b8b8b3e98e9ee95f418`  
		Last Modified: Tue, 08 Apr 2025 10:39:06 GMT  
		Size: 37.7 MB (37689466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc22bbf78422e9db07a2cd7f8daf44e6c7690e64987a9e8d2494ab04958169`  
		Last Modified: Tue, 08 Apr 2025 10:39:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320b063604e60e94d5e2bb889c9818fe731b742c4de7c007df1e1207c5f0f77`  
		Last Modified: Tue, 08 Apr 2025 15:46:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ffbd3c0537ee938903206c92f55a85da748f67d8eafe7bd1dee248ef27dc49`  
		Last Modified: Tue, 08 Apr 2025 15:46:28 GMT  
		Size: 120.4 MB (120407457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bee94135342a5901aae85d20f10504a03aeab01ab84df498768d9d1c045914f`  
		Last Modified: Tue, 08 Apr 2025 15:46:25 GMT  
		Size: 1.1 MB (1076188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903377b03eeeaee2e57c4e48bf370b4b1b09a8a710388a9ee9cc14aadb03e405`  
		Last Modified: Tue, 08 Apr 2025 15:46:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1ec62dc414b9396f60ac274f43a868a21be5f69dcedf4295cd8c48ddcad6bc`  
		Last Modified: Tue, 08 Apr 2025 15:46:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccfa295b25e1ba38393ff69149d98e3e1172da5a257c2d161d3251ad1f656d9`  
		Last Modified: Tue, 08 Apr 2025 15:46:26 GMT  
		Size: 4.1 MB (4056917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d981403815e949448d1a336818eb1dc33c66ee02f6edae4ca126de0cf91d8d82`  
		Last Modified: Tue, 08 Apr 2025 15:46:28 GMT  
		Size: 56.6 MB (56619537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407d125a235b3aacea4660b2ffeec7796738d6f811ab27afc18b1e1ca831c24`  
		Last Modified: Tue, 08 Apr 2025 15:46:27 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:b93fc5b82819b873f338a5b577ce095f8d7ff582eb86ac47bc9f6eeb87f1eda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1eb04d3a4938c04b09a5eb1ab6fc64f8266b38c7eccf3ba6ec5615ac38da0e`

```dockerfile
```

-	Layers:
	-	`sha256:d6b08564de423026161d113cbc99fa1ae8ed58f8359448b91330af2cd858446c`  
		Last Modified: Tue, 08 Apr 2025 15:46:24 GMT  
		Size: 41.5 KB (41479 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; 386

```console
$ docker pull redmine@sha256:c3e12f20584fd5f563ece23873eb3df4800ad5fb2e28afe2755b021bb0bcea92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253220954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572b4a0d3fbd18f22dd03d162f8225abf8f31bbef72545bad38ef598a3354a95`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 11 Mar 2025 02:53:30 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0287f848ebef97d1c4e63c30e137d2dbec1b399cabe85e8d8d913ff55f12d07`  
		Last Modified: Wed, 09 Apr 2025 18:33:22 GMT  
		Size: 3.5 MB (3503444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5783e87adb2a26f646f329232f3c38cb6ff063ae18aa5290c622b65b8bc968e7`  
		Last Modified: Wed, 09 Apr 2025 18:33:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016d425fa16044e0813531495882fd88abe8aea307ade0e364cb0c2697a26bb3`  
		Last Modified: Wed, 09 Apr 2025 18:33:23 GMT  
		Size: 34.1 MB (34083415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8004df2fb8f88d1a88be807c02c2018934b51f27269fd9fa008c9636878d2`  
		Last Modified: Wed, 09 Apr 2025 18:33:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc3d92a786dca31cca4ff525794817876c35d53daac5c1bdedc329173dede8c`  
		Last Modified: Wed, 09 Apr 2025 19:05:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34145e9698db7ece59f5afcd5f6823148570d1035d70f87719818e9d9b972ff`  
		Last Modified: Wed, 09 Apr 2025 19:06:08 GMT  
		Size: 125.0 MB (124988777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d2d45c30ea160682343b60eb52867cdbdc9369ba5492b9bcbc6227c13aaab2`  
		Last Modified: Wed, 09 Apr 2025 19:06:05 GMT  
		Size: 1.1 MB (1119111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf606bee67367cc45250314f1a799168c5e296fda7d8913f02dbcf05fe114fc0`  
		Last Modified: Wed, 09 Apr 2025 19:06:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978bf15dcd576dcd3055b67cf7924655289dcfa71bf2e884e5d304087c5177dc`  
		Last Modified: Wed, 09 Apr 2025 19:06:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d1243871d540417b70950f04f9f147eccd3df4ca6d292e70219a83a6812db`  
		Last Modified: Wed, 09 Apr 2025 19:06:05 GMT  
		Size: 4.1 MB (4056918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002af367cb6b761416ff5a0867a1f08c643c4055dd86a8f0da43eb3c20cd29f`  
		Last Modified: Wed, 09 Apr 2025 19:06:07 GMT  
		Size: 56.3 MB (56254549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdd2e734e873064aafadf948a44962b2b3641523f89e4152caf502563794e4`  
		Last Modified: Wed, 09 Apr 2025 19:05:46 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:8bfb1fe365a2944b416301c072041d232881e0030b990dbfdb16d884dcfed8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbb4e2c1b3a8e456b7bb3ea520038ff75e8e55d6a1d43c56f54487936da20bb`

```dockerfile
```

-	Layers:
	-	`sha256:c729589361ec7d30c27dc2f57f1ab866d31532c43f20f75d89901e0291ed5427`  
		Last Modified: Wed, 09 Apr 2025 19:06:04 GMT  
		Size: 41.2 KB (41190 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:78353cf20a45dc49185839ed51c31bc15ecbc218b6fb3eb8ec7c385dbfa37f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258997961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f1fa0a16b78720c768567b4db362f046a1b3b1b62278cfd9c133cd5ff8159d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 11 Mar 2025 02:53:30 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6949d2412d1813d925526134f33bbbd4b60e21f566ca57a9d89acc7ac2b8b0d6`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 2.9 MB (2895366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e679c23172564d07cc62e0bd6aeee3fc7a2046ca2bc38db85f21a647adca5317`  
		Last Modified: Wed, 09 Apr 2025 19:34:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384e4e692588a7faa303697fe06dffd3793d970dbaa24e5c7f3701cdb83a1f9e`  
		Last Modified: Wed, 09 Apr 2025 19:34:42 GMT  
		Size: 35.5 MB (35456435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae6c2379962f8e149e8e24dcb63c6c64268a9c5c87569ef3756ec2cfbc872a6`  
		Last Modified: Wed, 09 Apr 2025 19:34:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028d77c355749e31034755d77e7ec85b9a10d374602a1ba41c1c161e6590406`  
		Last Modified: Wed, 09 Apr 2025 20:23:36 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212711be66aa17b7d1dce226ff9d1ece9587ab56835b8711e6b149132dc2e67`  
		Last Modified: Wed, 09 Apr 2025 20:23:47 GMT  
		Size: 118.6 MB (118606617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecb68fd53d4b7634bc3044ffef064c251a68a7d8c12ab9a1cf846abdfca52c`  
		Last Modified: Wed, 09 Apr 2025 20:23:36 GMT  
		Size: 1.0 MB (1030880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47225608ef77d8694a6ccd7252d798e3c86344cf2e4ba88573e8430f3fb5fed`  
		Last Modified: Wed, 09 Apr 2025 20:23:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27c984369eb512dc7d8fd800307b78cd43a95fd5ceabe425d370748b03175e6`  
		Last Modified: Wed, 09 Apr 2025 20:23:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa192b0045dc5be95cdb14323fb1cc9f6f788bd03d4c0ab24e26aabb4b2e1e4`  
		Last Modified: Wed, 09 Apr 2025 20:23:38 GMT  
		Size: 4.1 MB (4056919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac53a5524cb63bbd726fae3efd0cbe2c33b3b899aaf790fae4950270ef79077`  
		Last Modified: Wed, 09 Apr 2025 20:23:44 GMT  
		Size: 68.4 MB (68433779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd04b24a16614f8f53751c31b42a40fce602bb741ad06ce62b75ae533651079`  
		Last Modified: Wed, 09 Apr 2025 08:39:50 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:98d1d5ea58129abe98c6758ac96fe77697d8d09bbe42d519c4495fe973ece8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519b1fcc1c279e386cd9e1085395c44231a6dd64ceec3c6609b03dcaab51992f`

```dockerfile
```

-	Layers:
	-	`sha256:95a36d0a8aa4a9db38168106e86f12f8ca932c5f1b158f4d6de3fdfbdf71ee2c`  
		Last Modified: Wed, 09 Apr 2025 20:23:36 GMT  
		Size: 41.4 KB (41369 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:deef9360c7b8a7a0f2c16206d6e04b4be3d6598a3ece5a062ef3ad4274fcdd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276109421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ff08c8c59a1450632e2deaeb626f752b25b6734a712ea1b8c2db6a56204fe9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 11 Mar 2025 02:53:30 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6d12ecbe65638512a1c6d62e733b6280e655439e06aa1632c31da30928df79`  
		Last Modified: Wed, 09 Apr 2025 20:02:05 GMT  
		Size: 3.7 MB (3702900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31799ee43564a6794e70342c80c681ff206fcd610d1bff64cdb6c07f579a1b2c`  
		Last Modified: Wed, 09 Apr 2025 20:02:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a80eca1c842bfc2b8240c91e1e0a975f302823afb710817e7f1ce5e2c7f83f`  
		Last Modified: Wed, 09 Apr 2025 20:02:06 GMT  
		Size: 35.8 MB (35831860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cec0e21d8573b94b50de2875e108d9c13f6dcc84c44bd145714ff53de598b4`  
		Last Modified: Wed, 09 Apr 2025 20:02:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a54432721a0c3582a59531a7eef7f5ef2f8df569e6112452770de4847e8815`  
		Last Modified: Wed, 09 Apr 2025 20:30:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed5334d3ce1c27e1ea10046b76d267ceccc07a7bd044309462433558b3a615f`  
		Last Modified: Wed, 09 Apr 2025 20:30:36 GMT  
		Size: 130.1 MB (130107826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8093f516b0d93bed220946dd0c6add3ee1e550e564dce77341c6b1729062ca`  
		Last Modified: Wed, 09 Apr 2025 20:30:33 GMT  
		Size: 1.1 MB (1066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3497a9a06323059fd7e83421dbab3dd727f4415a077795cfa2a8d4b9f76a06`  
		Last Modified: Wed, 09 Apr 2025 20:30:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7617ae16b3366ca1e2a6a2a36f69fcf20aadd994bc3f326f832ddf8b433add2`  
		Last Modified: Wed, 09 Apr 2025 20:30:33 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392242f4845b421cca7c99e4717d2df2676c5c919b8dfe82ffe7e569ec1f8fe`  
		Last Modified: Wed, 09 Apr 2025 20:30:34 GMT  
		Size: 4.1 MB (4056919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce1f9778f22b250cac7c2a9ba2f2b9bc351cd4f36f1d36ad4988fa96073e27`  
		Last Modified: Wed, 09 Apr 2025 20:30:36 GMT  
		Size: 69.3 MB (69271410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3fa24766e87905bb8641e4dec42e50ca04d54e4f1f5eab231ba56d22eaaa80`  
		Last Modified: Wed, 09 Apr 2025 20:30:34 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:73901a68bd2fe61a16714443a555ceddb61c9ec421c0d59dee2815df0b2ca412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a568f99e2fc211997a07561bab95d7b0b74da7046fcbb75c9d16e9c861f210`

```dockerfile
```

-	Layers:
	-	`sha256:cd5b5c01304d56b4790f09a1dfc84892694b046ee54ab8fbfbb314d41ec98bb3`  
		Last Modified: Wed, 09 Apr 2025 20:30:32 GMT  
		Size: 41.3 KB (41329 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:2f65268b566af4b18bc7bad7d1a9cdda55bd0d9aa9ea273b985c1567eaaeb5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256398124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc0d6e4be2caff9d652db85414c0494c62c732388b74340f66699ab46249e12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 11 Mar 2025 02:53:30 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eab93e0d63305db3d497c95992dbd3d14b93d5e0c2cbd97f4a8edfbb428aeb`  
		Last Modified: Wed, 09 Apr 2025 19:50:58 GMT  
		Size: 3.2 MB (3163370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6d57c9308909d37fe4ca9370b1a6830908cbc892f4a346e2bc4293cafcbc0`  
		Last Modified: Wed, 09 Apr 2025 19:50:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d8454546debdf76dc82bb54a14a929301b956bb9736835181ee7f22a5d2cd`  
		Last Modified: Wed, 09 Apr 2025 19:50:58 GMT  
		Size: 35.1 MB (35080754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c80021a8b68a83e52496e0ad2be5c91d0067f1992c4a6061c611f0cf904b7eb`  
		Last Modified: Wed, 09 Apr 2025 19:50:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabc87ecd5aec0ed7ce1cd797c00e4d24a5b5f758cfc5b979d2849ac4abcc32`  
		Last Modified: Wed, 09 Apr 2025 20:22:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cbeb4f330950ef6bdb50d1e04b64660bb42de3c71524757d60153791df2861`  
		Last Modified: Wed, 09 Apr 2025 20:22:03 GMT  
		Size: 118.8 MB (118779581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dbb88a345dd61cd4a89c2bc23e6efe6e8151e98471c1a6919e8d1bbd95852e`  
		Last Modified: Wed, 09 Apr 2025 20:22:01 GMT  
		Size: 1.1 MB (1108774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3251711591c2d98edc9f5fb448753453b78e8d6b76786c96553507e820a762ea`  
		Last Modified: Wed, 09 Apr 2025 20:22:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ed164a12452ef03a17b2dc856bd43248964be3302b143ef72234290403b38e`  
		Last Modified: Wed, 09 Apr 2025 20:22:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b192708df53e115f9799a2e3a0ed04a29c7da71267942771a01fee2460cc9aed`  
		Last Modified: Wed, 09 Apr 2025 20:22:02 GMT  
		Size: 4.1 MB (4056920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b878fb304c44a5fd3a06840de25b5df1acf7863ddccfab38023129a750b99170`  
		Last Modified: Wed, 09 Apr 2025 20:22:04 GMT  
		Size: 67.3 MB (67320110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650c6c73085e8ce3a7688207c8c0fd0953f78ad17b31166c90da11e25f712677`  
		Last Modified: Wed, 09 Apr 2025 20:22:02 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:d0b6e578bd9e05297169373dd8d0bcc81d1968131695eaef98082d51b8b02ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d2c3587627c786a0669cf19e7d0695c62287260e9fb1cf51b0857a2aedaf4`

```dockerfile
```

-	Layers:
	-	`sha256:f6a5b9348e56a130447c2bac375879cb109f4a60af37dfb2edcbf69f0b0c883e`  
		Last Modified: Wed, 09 Apr 2025 20:22:00 GMT  
		Size: 41.3 KB (41252 bytes)  
		MIME: application/vnd.in-toto+json
