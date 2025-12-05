## `redmine:5-trixie`

```console
$ docker pull redmine@sha256:3f27a1f91bc9dfb05495e3722a2c1bcd831acbc75388a4babb19ed584851d14f
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

### `redmine:5-trixie` - linux; amd64

```console
$ docker pull redmine@sha256:45cf063728428f54e70c1374834b9e32fc5893ad75838fcca317253a766f4047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236973937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824b7d9a87cb5200b06d72b7746dcad02805c9e97d3b5fa5dd8b6f2a3b08fcaf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:01:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:01:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:17 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 06:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 06:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 06:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:18 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:07:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:07:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:08:04 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:08:04 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:08:04 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:08:04 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:08:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:08:04 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:08:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:08:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:08:04 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:08:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:08:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:08:38 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:08:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:08:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:08:38 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:08:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec998db99e53b35a590a6789f001d95ade09ed6584562cb3e342f38adde7f701`  
		Last Modified: Tue, 18 Nov 2025 06:03:31 GMT  
		Size: 1.3 MB (1279387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f07c07465b2693735a6d011d3163c6b0e49cf656ffd1f4f20ec14b36a5b70a`  
		Last Modified: Tue, 18 Nov 2025 06:03:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f87030b2fa3d4fbf8cc2cdc9dd9815c76c7981db6a4f663b95fc19230b4b6c`  
		Last Modified: Tue, 18 Nov 2025 06:03:33 GMT  
		Size: 36.6 MB (36561122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924cdeb36ac5e8c240cdf88fdcce1582cc7f3b64d526ab2ac73106381e2ce3a9`  
		Last Modified: Tue, 18 Nov 2025 06:03:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db68a0a6a9458eefbb63e5b9bdb8be71928cd564ab77a79d88b0df5763bec1`  
		Last Modified: Thu, 04 Dec 2025 20:09:01 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab97cbc4b7348c4f81cdc9d1b7acd84639c3b6c3edd78500f0d7c11a90336de`  
		Last Modified: Thu, 04 Dec 2025 20:09:12 GMT  
		Size: 110.0 MB (109956002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f62ad413d75eee5a8d7311890ee2b439346f9c6a231b8e4f24c9fa1e063bd`  
		Last Modified: Thu, 04 Dec 2025 20:09:01 GMT  
		Size: 950.6 KB (950575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9c62285a672b744bb5d21f7badcab11f7beafb33de0c43b2edb8950ce62ed`  
		Last Modified: Thu, 04 Dec 2025 20:09:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc50f5c3f1ae0f9ffdac0e70f88b954be02eea7ea20d16903e6a6792330be37`  
		Last Modified: Thu, 04 Dec 2025 20:09:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2998de70a01df7fd94bc7724f5b4565cc6d3ff38acb631a2fef5efe1419f970a`  
		Last Modified: Thu, 04 Dec 2025 20:09:04 GMT  
		Size: 3.3 MB (3250748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72672aced77633b22753bad170065122b4274c12b86938cb8bbf78bfe467db87`  
		Last Modified: Thu, 04 Dec 2025 20:09:10 GMT  
		Size: 55.2 MB (55195501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05973792c80a041e0edffabbbb24fe0709ef21e9f25393665029756a299a43a5`  
		Last Modified: Thu, 04 Dec 2025 20:09:02 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:7737810e73e9d4ff0ba3720b43115575a8b163fae65d994906ae643f0e04b4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d4b190b7ce341358d38df32f4e148eb10a73ef5ab3bcb41353bac64341519a`

```dockerfile
```

-	Layers:
	-	`sha256:40f44ea99802f61b02a7537fe2a18263abd3c514f96429aa369ddb5305580421`  
		Last Modified: Thu, 04 Dec 2025 23:49:46 GMT  
		Size: 40.6 KB (40592 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:3c3e9265e179eed5ee81399dd058c2610f6b2ebbf4bddd69224b995aa15b8dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224423160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf47f37e883d7e8db6983aaf697ebe29ecfd25f02fa532629ea47750b52bc32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:21:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:24:25 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:24:25 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:24:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:24:25 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:24:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:24:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:24:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:24:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:24:25 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:06:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:07:03 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:07:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:07:03 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:07:03 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:07:03 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:07:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:07:04 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:07:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:07:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:07:04 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:07:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:07:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:07:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:07:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:07:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:07:48 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:07:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517c7bd9d55813db5acd8b006c28017e3c4b85d7faf3f682b7874db4b8bcd08`  
		Last Modified: Tue, 18 Nov 2025 04:24:40 GMT  
		Size: 1.3 MB (1263012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141ec2aeb888d8fcf3ce3e258e90bfb6e4bec4f2d1b2fe594019f50942e41ba`  
		Last Modified: Tue, 18 Nov 2025 04:24:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e71c4146227b2d612085fbcf714d7e27ea90fb8c3ad7d5b55b39d8f2f7465e8`  
		Last Modified: Tue, 18 Nov 2025 04:24:42 GMT  
		Size: 32.9 MB (32923073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c658a9362aa864d8b62ffb571466fdfcf5bf5dda01160e35ce4784bd773a4`  
		Last Modified: Tue, 18 Nov 2025 04:24:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384c7a9d52805ae546b7756f57608b47d20b3814a049e64491d5f773bc4d9228`  
		Last Modified: Thu, 04 Dec 2025 20:08:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a6bac0b5d9d7641161ed0b5b6cc4ef53d077c4a6f5ccc2c4222f8a667cccd4`  
		Last Modified: Thu, 04 Dec 2025 20:08:22 GMT  
		Size: 105.8 MB (105782335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3125a423679ed7e84a4d5bfca3d8c9c9b099052e01a83edbb3a6793a1d1af3`  
		Last Modified: Thu, 04 Dec 2025 20:08:10 GMT  
		Size: 919.7 KB (919727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993c5e61cc339e1ba2c44012396afdada357ecbd65111a591f2c69af13628a11`  
		Last Modified: Thu, 04 Dec 2025 20:08:10 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485034d29f906e630280b6cc4ac042108f7fe2d2601d75cd98574c6d854547b`  
		Last Modified: Thu, 04 Dec 2025 20:08:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9086fd081fbfa9ed5e219181c34b87408641992d40020480bd1be1831e490a`  
		Last Modified: Thu, 04 Dec 2025 20:08:11 GMT  
		Size: 3.3 MB (3250746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c4d97263fa4f93b9b7c855f52c8f85a00101ebd7ce4aa147ee3d7ca5001fd9`  
		Last Modified: Thu, 04 Dec 2025 20:08:17 GMT  
		Size: 52.3 MB (52336001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d47a6f1e5ebc8dfc7747310f4e3b2a8c30a16e9f045c5f72c8f69b43e7292b`  
		Last Modified: Thu, 04 Dec 2025 20:08:11 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:9d513232e541aa1517169613f5a3919f966debb12c0b00d4bad981ae3170d7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd07d1e4c805581034622824714f3df830d2d8d80875a2e93e621684ab61029`

```dockerfile
```

-	Layers:
	-	`sha256:dc6bee157f78f7879edf60215bf9cf047b9df17a7e456f2980b39332b95cbd04`  
		Last Modified: Thu, 04 Dec 2025 20:49:26 GMT  
		Size: 40.8 KB (40753 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:3c8eb4eb9af7172ca7e03c437208bf5e1957201c1568bf7cc3ff948e3b362dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217311965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8b7c45171597a3c3a623221d3f64226e05c9125b738809e9303655790ed5a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:01:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:04:10 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:04:10 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 05:04:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 05:04:10 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 05:04:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:04:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:04:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:04:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:04:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:04:10 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:08:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:09:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:09:30 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:09:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:09:30 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:09:30 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:09:30 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:09:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:09:30 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:09:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:09:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:09:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:09:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:10:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:10:11 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:10:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:10:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:10:11 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:10:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90634663f9f573b081adda1092fd94780640cbcc3c6de46429d190333c2ebe4`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 1.2 MB (1236532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005803ec545f1bb33fd98e24607619a32192923ec513ebb2353ab2e57bbb8b9`  
		Last Modified: Tue, 18 Nov 2025 05:04:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715ac483c22dbe78ad082569fce2526c0a95f01875a50606d8fe561b0a073ac0`  
		Last Modified: Tue, 18 Nov 2025 05:04:32 GMT  
		Size: 32.8 MB (32803816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012e835156a4932b97e081b7f360bb618469bb692946a201e136ffa1a9c19d21`  
		Last Modified: Tue, 18 Nov 2025 05:04:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b124552f1fb970f3999f976a7180820283f92db4192267077179aa2d8e2bd02`  
		Last Modified: Thu, 04 Dec 2025 20:10:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e908dff1ee391d5b3acdb3753acb024e709390ac88afa65c49c45fe7851593a`  
		Last Modified: Thu, 04 Dec 2025 20:10:46 GMT  
		Size: 100.7 MB (100674804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610a5c21fe84e68920dd512d5edb9bbbf3b076173dc9f13521f8c9acf593d45d`  
		Last Modified: Thu, 04 Dec 2025 20:10:35 GMT  
		Size: 915.6 KB (915617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54959e6cc98bb886f27d8a7863a30d3a3970917c1d2bc3379cd4e8c02601e39`  
		Last Modified: Thu, 04 Dec 2025 20:10:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff475aa7b5eba32b0c5f7c47698cc10e6cabba5bb64f9c93d8f17f12330ea5bc`  
		Last Modified: Thu, 04 Dec 2025 20:10:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6290009b468a7e181b8fa9436d0b0d51332b2bb24a02f41b61fdc1620851db`  
		Last Modified: Thu, 04 Dec 2025 20:10:35 GMT  
		Size: 3.3 MB (3250751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d1d4a9b794c68997d000e4e809175421049d67a396461a71b4b9ec451f1bfc`  
		Last Modified: Thu, 04 Dec 2025 20:10:43 GMT  
		Size: 52.2 MB (52216369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beef0a7124ce0df039db2a42ae795b25534a9e7b11c112411695357504f9182e`  
		Last Modified: Thu, 04 Dec 2025 20:10:34 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:6881b664783dbd4e31596d7da55d77261890d28e29173c4093d9d6f1163e0daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe2c27b7d15ce39b4a9597185313ec116f74a98ff5e27d70314d05e21b7638f`

```dockerfile
```

-	Layers:
	-	`sha256:93e50d50f2733f0e08fcc9df7e02e025157ddcdd835979f2fd82b0a47c291c74`  
		Last Modified: Thu, 04 Dec 2025 23:49:50 GMT  
		Size: 40.8 KB (40753 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:6ae60bf761f3b871ee251658d38ad6af7d31be6ddca0f74de595fee39f31e852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235035397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbe47d2c214f8e7bdbc80ef2c2bec7e09bb709e70f24801a87409f0c29fa0e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:46:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:49:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:49:14 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 04:49:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 04:49:14 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 04:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:49:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:49:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:49:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:49:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:49:14 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:11:03 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:11:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:11:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:11:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:11:37 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:11:37 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:11:37 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:11:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:11:37 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:11:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:11:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:11:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:11:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:12:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:12:12 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:12:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:12:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:12:12 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:12:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ead93ac0086528b64d43bd59ca36daecde7bad37faf5d852c21df69a9b7e5`  
		Last Modified: Tue, 18 Nov 2025 04:49:29 GMT  
		Size: 1.3 MB (1261688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e4e2bc4753a006ae658bb77b4fb654065452d9f3b489e20ad6ec00121af4c5`  
		Last Modified: Tue, 18 Nov 2025 04:49:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438be3edc404073b6404edf90ee16966ee2205cfd151e6d27c36d489cb5eb82`  
		Last Modified: Tue, 18 Nov 2025 04:49:41 GMT  
		Size: 36.5 MB (36537463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1448e52bb65ab9b9b15c5e90e757dbff403616189fdf864fd3545e863217c`  
		Last Modified: Tue, 18 Nov 2025 04:49:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eec7db40b5db143dfebd4b06f9a61ee0aed0cb2bb70d6da1919584c67d1b1`  
		Last Modified: Thu, 04 Dec 2025 20:12:37 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf69f25dc187d04dcc3453d945c111515a15d486bab2e71ad24982e970362d`  
		Last Modified: Thu, 04 Dec 2025 20:12:43 GMT  
		Size: 108.4 MB (108375764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b0be5ca3ceedea40dbd5712329d5291f2044e0899a302f7811a49e5691d8d`  
		Last Modified: Thu, 04 Dec 2025 20:12:37 GMT  
		Size: 903.5 KB (903460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2f3b65c7397ed3b5a18b4f1259860827a02e9573d9a98eba3279c3620480bc`  
		Last Modified: Thu, 04 Dec 2025 20:12:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892e2f081bc7cd9b10a47de52852255a68ea27eee983d7f08ddf188b4ececac1`  
		Last Modified: Thu, 04 Dec 2025 20:12:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472dec650ea3c66fd9332d92b234b63f5a4baedf3d4dac3703197827dc7deaeb`  
		Last Modified: Thu, 04 Dec 2025 20:12:38 GMT  
		Size: 3.3 MB (3250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38847ce64d1f34879a249196d773368d8cbf139fc4b0c4da2910436e094f37a2`  
		Last Modified: Thu, 04 Dec 2025 20:12:59 GMT  
		Size: 54.6 MB (54563540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab82536a6868ab1d01e27eb4d3f85aabb6ab5d5a6509f30d23ab56ba4574cfe4`  
		Last Modified: Thu, 04 Dec 2025 20:12:38 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:411c5b07d0756d34fcf0b445e0006be34311a2b34652a260942a54d397c7f5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ad7bb8a37ebc9ec8afc3a2bd5ee740b5273d7f1e77c86b0efd0861cc36be6f`

```dockerfile
```

-	Layers:
	-	`sha256:6b6fcfeea982cea44f443e6da95acc6cbdc989a2644a328e93a9a3a0dd350998`  
		Last Modified: Thu, 04 Dec 2025 23:49:53 GMT  
		Size: 40.8 KB (40795 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; 386

```console
$ docker pull redmine@sha256:3026a658ae488d33271b491cb4f7a0271d4c5e7cf6a3fd1ea91d77ce302660bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236988773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c9a6797996fa63166f4c6861658c8575f4d3636836ceb5d03ad76cfab28867`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:42:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:42:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:45:04 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 03:45:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 03:45:04 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 03:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:45:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:45:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:45:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:45:05 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:03:18 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:03:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:03:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:03:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:03:56 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:03:56 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:03:56 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:03:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:03:56 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:03:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:03:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:03:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:03:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:04:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:04:38 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:04:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:04:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:04:38 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:04:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35370883866198ef7af1f9320add997b473b29301db2906afe4fa8e1466002dc`  
		Last Modified: Tue, 18 Nov 2025 03:45:19 GMT  
		Size: 1.3 MB (1287198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b666a3b431c0df3834928fd1b3283a91d4b9060da314e49233a85a97fbb999b1`  
		Last Modified: Tue, 18 Nov 2025 03:45:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f39707dc6b3193a4b34f0d070321072966ac4fd55debc400857e9e288670400`  
		Last Modified: Tue, 18 Nov 2025 03:45:22 GMT  
		Size: 32.7 MB (32706601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123c92f25591d84e92e657610e404392ff48ef50e78ca5017c5d7c6024a86a27`  
		Last Modified: Tue, 18 Nov 2025 03:45:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb1cdb56db20fd7af94b6fa946490956bbaa7e988566f35e9a12fffb1029a62`  
		Last Modified: Thu, 04 Dec 2025 20:05:05 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842244bd344a05fc3ddd78469a82486160af385695b5f43d2255967d70366c18`  
		Last Modified: Thu, 04 Dec 2025 20:05:20 GMT  
		Size: 112.4 MB (112445585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827b99cfedd4d2347093128df3c6b88d764ef156dd890c3002336f89930aa599`  
		Last Modified: Thu, 04 Dec 2025 20:05:05 GMT  
		Size: 918.9 KB (918919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db2d0336be0a7dd3a7c846e235dee46a1bf33474e17e42bd8be6750107eecd`  
		Last Modified: Thu, 04 Dec 2025 20:05:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4a0e73d2797918cf67b133af9f5804f4eccf6207ab4f90e185661913ef618b`  
		Last Modified: Thu, 04 Dec 2025 20:05:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a3d061e77e933660d144ffd3bd0c951dba6539443c1dc1a5262164d0180ff`  
		Last Modified: Thu, 04 Dec 2025 20:05:06 GMT  
		Size: 3.3 MB (3250757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167b081a054c4472bdfbb8607ab8d104169015811c6d7c81263858b13cab3a94`  
		Last Modified: Thu, 04 Dec 2025 20:05:15 GMT  
		Size: 55.1 MB (55082525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf769a76406bde65671f412992ee9c00885972d1e862f12e5813a3ad525f678a`  
		Last Modified: Thu, 04 Dec 2025 20:05:06 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:53b55a7d168a8bc1947627f3678f3d5022bfb03c0f4b2e8a0fb28a5ec0999e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 KB (40539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf49a851d449af292e1aca05c0ed795efb2c72178cf2aafedefcc424332866d`

```dockerfile
```

-	Layers:
	-	`sha256:14ff09233e31bbda3485ca11423f1669f4d76ec72e23e5951c06f1f757552b0b`  
		Last Modified: Thu, 04 Dec 2025 20:49:36 GMT  
		Size: 40.5 KB (40539 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:64b802508d9b4219406775376d4bfedc556167d6b45b3999cf17043c3eff5953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259214694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3cbf26975d04150352c04d0f246147f8ec62e161ae12d38f01f07f09a76d57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:54:49 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:54:49 GMT
ENV RUBY_VERSION=3.2.9
# Wed, 19 Nov 2025 00:54:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Wed, 19 Nov 2025 00:54:49 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Wed, 19 Nov 2025 00:54:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:54:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:54:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:54:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:54:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:54:49 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:33:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:35:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:35:18 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:35:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:35:18 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:35:18 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:35:18 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:35:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:35:19 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:35:19 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:35:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:35:19 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:35:23 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:38:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:38:46 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:38:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:38:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:38:47 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:38:47 GMT
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
	-	`sha256:8fc973e1a4f02b60e10371b7902c59338e2e60e10071ec32bf20a661fa058928`  
		Last Modified: Wed, 19 Nov 2025 00:55:18 GMT  
		Size: 34.4 MB (34397229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d071409c31b01235266463ca26ca047923cf742426684e0f57b58acabfff68d`  
		Last Modified: Wed, 19 Nov 2025 00:55:14 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f066c81f5d097d14a908220151834fe9e907ff58152abc5179cdb87439db42`  
		Last Modified: Thu, 04 Dec 2025 20:39:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf3f6572dc85949f77640b144be034f1cb39f2445531d1cd9870bf294079a7a`  
		Last Modified: Thu, 04 Dec 2025 20:39:42 GMT  
		Size: 117.4 MB (117410720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1162fe4e376fc730047e018a92ebc1b577c5850438c3381d0eb666351f74aaa`  
		Last Modified: Thu, 04 Dec 2025 20:39:30 GMT  
		Size: 909.7 KB (909686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d01950d0073ec14c43d391db9579ce7988e7cbae5ef05da8e943246b6f04c7`  
		Last Modified: Thu, 04 Dec 2025 20:39:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc831852c4cb4ba41abfb2f78ca77c3ceea6db5fa2944a817de09ea65d9a6f7e`  
		Last Modified: Thu, 04 Dec 2025 20:39:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430588e7a067430ae567b256f6cc38441c6bac822e4606431e62fa483e4f9b90`  
		Last Modified: Thu, 04 Dec 2025 20:39:30 GMT  
		Size: 3.3 MB (3250756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f1d6a5c1c9ca1b5b74739d65b4657b1bd9c4ba3a34021990f166316483c9a4`  
		Last Modified: Thu, 04 Dec 2025 20:39:38 GMT  
		Size: 68.3 MB (68335652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed438c4b6da7dc8facea9d3697fcaa29d7ad7499675957a464356251309c16fb`  
		Last Modified: Thu, 04 Dec 2025 20:39:30 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:63de8e59ee3ffb702324582e44dc42b52fe700f8ee629ff06d8493736e76676e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593739bf7cd06bb64fa8306d340aba5b06e45c460acfa3dfa6abb383d9b7e38d`

```dockerfile
```

-	Layers:
	-	`sha256:35b49e4ee0fe2be07eb72c20c99d01aa1729d79682631e8a2dacdeee1a961c4a`  
		Last Modified: Thu, 04 Dec 2025 23:49:58 GMT  
		Size: 40.7 KB (40658 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:1fc7fa290028cd15019425a9ee6ec8910c2cc571fc4281115fd996c9c28dd8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243206193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0fff158e8ebb0de5fddcf4a2d30e8da3aacbec2aaf767e3d04ee51ce5b8ba0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 13:00:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 13:00:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 20 Nov 2025 17:34:07 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 17:34:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 20 Nov 2025 17:34:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 20 Nov 2025 17:34:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 20 Nov 2025 17:34:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 20 Nov 2025 17:34:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 20 Nov 2025 17:34:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 20 Nov 2025 17:34:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:34:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 20 Nov 2025 17:34:08 GMT
CMD ["irb"]
# Fri, 21 Nov 2025 11:47:48 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 21 Nov 2025 11:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Nov 2025 11:52:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 21 Nov 2025 11:52:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Nov 2025 11:52:27 GMT
ENV RAILS_ENV=production
# Fri, 21 Nov 2025 11:52:28 GMT
WORKDIR /usr/src/redmine
# Fri, 21 Nov 2025 11:52:28 GMT
ENV HOME=/home/redmine
# Fri, 21 Nov 2025 11:52:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 21 Nov 2025 11:52:28 GMT
ENV REDMINE_VERSION=5.1.10
# Fri, 21 Nov 2025 11:52:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Fri, 21 Nov 2025 11:52:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Fri, 21 Nov 2025 11:52:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 21 Nov 2025 11:52:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 21 Nov 2025 12:42:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 21 Nov 2025 12:42:31 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 21 Nov 2025 12:42:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Nov 2025 12:42:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Nov 2025 12:42:31 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 21 Nov 2025 12:42:31 GMT
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
	-	`sha256:7f94d11db2ea22d4fcf35771507592846b2db06aa0011454772bba0dae6d4228`  
		Last Modified: Thu, 20 Nov 2025 17:35:58 GMT  
		Size: 32.7 MB (32739264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abccbd3d65208f971b9126d47150eedc1af1a4ab8b43175c517cbf31fc5d5a3`  
		Last Modified: Thu, 20 Nov 2025 17:35:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee87084ccf1d5da8817e129afc1605f19ccea074f33dafb5127e0aed39aa5f`  
		Last Modified: Fri, 21 Nov 2025 12:45:49 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7a23cc29286d7834f97f3947bd1d21ed6b5b22847c4d28dcd63f6d3ac52614`  
		Last Modified: Fri, 21 Nov 2025 12:45:56 GMT  
		Size: 107.2 MB (107226756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bcedf789b9f2c47e94d455c79829854adbbb046cbe6f79a37194340a034e9e`  
		Last Modified: Fri, 21 Nov 2025 12:45:49 GMT  
		Size: 896.7 KB (896681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668ee163e553cc1819bc580156189f84cc0162c544d185c4a387b6c268820b8a`  
		Last Modified: Fri, 21 Nov 2025 12:45:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a3f347e630a4055d84ddc5d5d5af33b623516142a7b991b27d95d15355aac`  
		Last Modified: Fri, 21 Nov 2025 12:45:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de34070ad09d4482173c6f780dc7f515634380b39fe3d9e36447cedd8f69dbd`  
		Last Modified: Fri, 21 Nov 2025 12:45:50 GMT  
		Size: 3.3 MB (3250780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aa7bef2a258acf2a396de2a1d1499d60dad96ed51ba6a67c127b127f7531c6`  
		Last Modified: Fri, 21 Nov 2025 12:45:53 GMT  
		Size: 69.6 MB (69567551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1e944c662aaf25524b4a1b1621573199a0eb935208c912ff0c64bf8aadb108`  
		Last Modified: Fri, 21 Nov 2025 12:45:51 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:27f73c114a3f0cc36613f94890af63b69740ca689079df626909bb8e5cfcfd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38497a42b6e931dd2d109eb12f6a2c1e3595ead21ffa3e65562fa9fb7227032e`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb9b6cf2a494c756635dfeaa2cc41dfc3f304c3c02be019afc87f5ec6c58d1`  
		Last Modified: Fri, 21 Nov 2025 14:49:37 GMT  
		Size: 40.6 KB (40574 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; s390x

```console
$ docker pull redmine@sha256:2074c75972ed3bec6c594213a2ed38e94a433df8ec63a58252bf4495bdd2b070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247396154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210d484c4e534ed3a2a9135e96c9d5ca0bd32fba5f683f010177af480a1f3817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:19:49 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:19:49 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 18 Nov 2025 05:19:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 18 Nov 2025 05:19:49 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 18 Nov 2025 05:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:19:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:19:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:19:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:19:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:19:49 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 20:15:58 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Thu, 04 Dec 2025 20:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Dec 2025 20:18:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 20:18:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 20:18:28 GMT
ENV RAILS_ENV=production
# Thu, 04 Dec 2025 20:18:29 GMT
WORKDIR /usr/src/redmine
# Thu, 04 Dec 2025 20:18:29 GMT
ENV HOME=/home/redmine
# Thu, 04 Dec 2025 20:18:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 04 Dec 2025 20:18:29 GMT
ENV REDMINE_VERSION=5.1.10
# Thu, 04 Dec 2025 20:18:29 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Thu, 04 Dec 2025 20:18:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Thu, 04 Dec 2025 20:18:29 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 04 Dec 2025 20:18:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 04 Dec 2025 20:22:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Dec 2025 20:22:12 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 Dec 2025 20:22:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 20:22:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:22:15 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 04 Dec 2025 20:22:15 GMT
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
	-	`sha256:aefc54ab310ea610a2d51f93a192f835cfc96f83a04d29e48ce4361fa2ee1fbc`  
		Last Modified: Tue, 18 Nov 2025 05:20:11 GMT  
		Size: 34.1 MB (34066734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148ddf9b30063ef0eda5e27c017752058605db04139d7fd6752b095a44778f3c`  
		Last Modified: Tue, 18 Nov 2025 05:20:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b8eca7c2cce601ed71ed683ff72f6aa2803a6dee0a30793343781dc92609c`  
		Last Modified: Thu, 04 Dec 2025 20:22:58 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7565052a806b38f3912fed543a70638928e37937cdaad9fbc4f98505f0a6e31`  
		Last Modified: Thu, 04 Dec 2025 20:23:10 GMT  
		Size: 110.8 MB (110763077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2a743ca69ca02ba064389e7442db9abc45b15bea619d93a12cfa977a93ec1c`  
		Last Modified: Thu, 04 Dec 2025 20:22:58 GMT  
		Size: 923.2 KB (923167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005f241ef09d06f40e354a6785bb05ae7ebf9d41ce4734f666ec8fcc0c39c79`  
		Last Modified: Thu, 04 Dec 2025 20:22:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e22e31062ff86784ea2d64e26c07ed579cbf8ada968157f2d11a82a3c771639`  
		Last Modified: Thu, 04 Dec 2025 20:22:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7436d50ae818a595a9f4885590e7c99901d32654867a7ba275fa62b8235f3a3e`  
		Last Modified: Thu, 04 Dec 2025 20:22:59 GMT  
		Size: 3.3 MB (3250744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b6913a04eaf87bdb12cf8a7559d92facdde8e473b3c1e46b059739aa2bb3a5`  
		Last Modified: Thu, 04 Dec 2025 20:23:07 GMT  
		Size: 67.3 MB (67259687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e2366c65efc6a9637f0ff6c95c48bd56447373e95c00e8730bdaedef4bf3b8`  
		Last Modified: Thu, 04 Dec 2025 20:22:59 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:e5a78bc8886997ef023e0f6bc0eeeed1653181c6b01b4b741b18568767a5ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b69b53fd4435516ff194d7a36a45b1b746b810b84257ca5e3bc352a75a42e3`

```dockerfile
```

-	Layers:
	-	`sha256:dcb6d37b6f1916be9a91a5d8fba1008eca3c99a7cfadcf85093308ec311aa7f8`  
		Last Modified: Thu, 04 Dec 2025 23:50:03 GMT  
		Size: 40.6 KB (40592 bytes)  
		MIME: application/vnd.in-toto+json
