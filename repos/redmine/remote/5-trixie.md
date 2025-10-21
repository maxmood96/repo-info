## `redmine:5-trixie`

```console
$ docker pull redmine@sha256:44f8a1417400b94d7421898fa778e018e94165b48a282578e4b430e330d55118
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
$ docker pull redmine@sha256:c25f222a97281cd76ab99cc4b1f62e1de1fe794f8991f70deb02465a801ea15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240363635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3aa55dbf3540ac61f55ffb8a02d322ea158316015726831afaa02b945e6eb2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b04bd290b240942780650e73db4aa4df47b12b931a2dbfbaa2de6217caf560`  
		Last Modified: Tue, 30 Sep 2025 00:47:12 GMT  
		Size: 1.3 MB (1279319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea96f17c6e2876317784948ef970774bd908f773ee32c5da6a2e6f500f6a6d7`  
		Last Modified: Tue, 30 Sep 2025 00:47:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3b3856680143254ba3d40bcb3c0ef06afbdb63bf45ebbdb148b6439c1f01d2`  
		Last Modified: Tue, 30 Sep 2025 00:47:14 GMT  
		Size: 36.6 MB (36561090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00617a8ed5eba41aa8b1f175b660b2b80fbd9378b83db7a23697ad1677cdfe63`  
		Last Modified: Tue, 30 Sep 2025 00:47:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c318468fc4b2da4295ddab72b78af57191bbb398bfee94e12a9615bd6f8fd2`  
		Last Modified: Thu, 09 Oct 2025 17:28:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4b279b4e703eb290438b0a6de80d81e9cce01b6e04044f22199010e9b059bb`  
		Last Modified: Thu, 09 Oct 2025 17:28:39 GMT  
		Size: 110.0 MB (109951305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9561d69cf06ebd11ce7cbcf8ce80881ff3165e3bbe79bbc7dd7120f3881a96eb`  
		Last Modified: Thu, 09 Oct 2025 17:28:31 GMT  
		Size: 949.9 KB (949943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385b728f8cef5fdf9ac8640759742a3f83b75405366be625575fcf6eadc66471`  
		Last Modified: Thu, 09 Oct 2025 17:28:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572b381c8a062ff934cb613c455a97b69abdef526212dd98364c3775a4b686ff`  
		Last Modified: Thu, 09 Oct 2025 17:28:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82beae386ff084b69dcd5f45ea51f22959e67d0f095f291d1ed37d193ef52a1a`  
		Last Modified: Thu, 09 Oct 2025 17:28:33 GMT  
		Size: 3.3 MB (3250790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a43c6fea7df5210b7f9c4c148f5128622bb7a1009c64f62bc988897eef5418a`  
		Last Modified: Thu, 09 Oct 2025 17:28:36 GMT  
		Size: 58.6 MB (58589303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7b8a0dbaf9dc8f3c60cfc252f8e77eba44280e7cd6a6667611d9ecaabb3e37`  
		Last Modified: Thu, 09 Oct 2025 17:28:32 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:6808e328d027201e263a8fa2157e8a08c52c3ebed4508e246530c08104a1117a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3b5bb13b67b9ba103c638e6ca47419a72b39bf1fb3e0ceeea8601043b1826b`

```dockerfile
```

-	Layers:
	-	`sha256:2fc20d4528f6d377c26a60c644c91b490779be54a113251d7b9ecda08142945a`  
		Last Modified: Thu, 09 Oct 2025 19:49:38 GMT  
		Size: 40.6 KB (40551 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:8c383d561f350bbf09b28452fe6abd108224f42c9d643bc70173ce9f444db56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224417985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d98fd5c907cebd1f1dc748436bad08d92b03cce28423caca2695615f4921dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd4d3de6a90f8d0f5faef22f559002a749471358c16cf37594dc28fb467a91`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 1.3 MB (1262887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117ed1c5d0138a63fe137788b666a0178d9f4d5284aed97a3214cb9626c2980c`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60113293634b8e53fc98110bc8382edd359eccf0df8907c2df69c19691cd79c2`  
		Last Modified: Tue, 21 Oct 2025 03:22:25 GMT  
		Size: 32.9 MB (32921519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cd7523ad0f9f8179b7c5109a9a5ba12d519ecc018c519b25cafdcd13573bed`  
		Last Modified: Tue, 21 Oct 2025 03:22:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2801e364d69438967fd9a05505926e16db8353d78d0232d31077ddef8a637a8e`  
		Last Modified: Tue, 21 Oct 2025 04:31:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a856528c0983a9a75a5040c62f7e0d0f37c24654564c8aba5a6087beebfa35`  
		Last Modified: Tue, 21 Oct 2025 04:32:34 GMT  
		Size: 105.8 MB (105781542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1553f52c18388b851c2424802424b0fd3f769605e534a4864be17ea30379049d`  
		Last Modified: Tue, 21 Oct 2025 04:32:17 GMT  
		Size: 919.6 KB (919629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f67f7132d24714a0f5cb9b4e11ee382d39e30293e806dca3cbdcdb556e463dc`  
		Last Modified: Tue, 21 Oct 2025 04:32:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecfe5da494c7dd30a02ec7e065d9a90622ac2b83b4e71d1fbc8e353e3e3dd8f`  
		Last Modified: Tue, 21 Oct 2025 04:32:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31916ee05e42ac3f9d9cb3d00df11e6155bb59cce126dc3f0c8a83d53c5a45e7`  
		Last Modified: Tue, 21 Oct 2025 04:32:16 GMT  
		Size: 3.3 MB (3250780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d10143b13b1244ccd4fbec6d914cdf43708d7efae462f92c36c1a7f778f3deb`  
		Last Modified: Tue, 21 Oct 2025 04:32:19 GMT  
		Size: 52.3 MB (52331228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f5837caf1607a4c3a82307ca3195260306cfb5f62062340aedfa0115ee9098`  
		Last Modified: Tue, 21 Oct 2025 04:32:15 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:a5f7c60d3e90b3d26d723b140f5e48f097f91fa35294a750c6c78d037fda93ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b744ad6860b545d7fb83ea67380142802e52c64442339b1fcf760b23c9eaadf9`

```dockerfile
```

-	Layers:
	-	`sha256:d55d47d2554f2033fda6596b6f5bb0235634944842b4ed3f284e525b88a6c882`  
		Last Modified: Tue, 21 Oct 2025 07:49:25 GMT  
		Size: 40.7 KB (40712 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0be85fa0b6ad988b12aba771eda7ba7f69eccbbfd02b99695b1163a5e4afb28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217306595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a80b6a52b91e1b713415ee921bea9fc0a0dc92311a1eae0ad1289ca960565c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba24fa59d3e1868caf49b2f68be6c0aa603a54e870457c69795d6f675112df5b`  
		Last Modified: Tue, 21 Oct 2025 03:52:43 GMT  
		Size: 1.2 MB (1236035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53718185c354eea978589e0ba9dcbecf5e6b316dfe6018536ad97fd461c6e67`  
		Last Modified: Tue, 21 Oct 2025 03:52:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969d6e3f582ee67d7de7c4b1770be9e3daef67de8e91c07afe6171247f7b4eab`  
		Last Modified: Tue, 21 Oct 2025 03:52:44 GMT  
		Size: 32.8 MB (32803650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab1b857a7f6c7aa39c31b412935043dbb35636fceb0aa899079c2f1b58dd8aa`  
		Last Modified: Tue, 21 Oct 2025 03:52:42 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8148b1902ef8cc9894db95bf03fbc6b7ef1698f9227611edc3da33a73e91d184`  
		Last Modified: Tue, 21 Oct 2025 04:39:15 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c12872878ed1aaa9c4e6e667a66275ae435810d1788b4cf72271cbb8f55760`  
		Last Modified: Tue, 21 Oct 2025 04:39:29 GMT  
		Size: 100.7 MB (100672943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f8a8b11cf1f4b1cdbc66734354bf4f7d780d76d26236776cb7a9934b41eab6`  
		Last Modified: Tue, 21 Oct 2025 04:39:15 GMT  
		Size: 915.5 KB (915514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b19f08c78d419fe574c429f6fbfee6c9d24795b08cd872ffffd15c2a54f4a`  
		Last Modified: Tue, 21 Oct 2025 04:39:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25401f91ea0e70b29f1e5afa0deb3a306d6d0df0c52a3101ca175008907ce35e`  
		Last Modified: Tue, 21 Oct 2025 04:39:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49e66d67484464f60bae0f6cfcc8ab317c0f93bdcf52420bce2392ae2e14da2`  
		Last Modified: Tue, 21 Oct 2025 04:39:16 GMT  
		Size: 3.3 MB (3250782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b978a6e1f87ad4080205d6539bbdf17de911a6e850cf65491327a508b1829`  
		Last Modified: Tue, 21 Oct 2025 04:39:22 GMT  
		Size: 52.2 MB (52210663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb51d4cb36bee571927de9daf2ed9d67ae846ef0275efc14a73108754eb3d4`  
		Last Modified: Tue, 21 Oct 2025 04:39:16 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:0f61c062d5b062226f12b04b25c3e27a69eb6e31156e20b85775db55f9099602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa90b45e7e49fd113556915227d6d70484917660dd094e25493fbeda92090926`

```dockerfile
```

-	Layers:
	-	`sha256:02238448f846bd6824fc455cb2dce058f39c96a77a2f25b556fe94ee86b55099`  
		Last Modified: Tue, 21 Oct 2025 07:49:28 GMT  
		Size: 40.7 KB (40712 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:d2a5cb636faa9f1889eba508a509764b23cadd5253763f3da433b3505a17e99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238777944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790f48347e34151a0037ba296d6a3c48f0ad3563c7cb7cafdb7f580b34dd376a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64c5a7ded79bb69b5af1cce6a8c2c34f7b604b85e8021a57dfc8986a7c6f5b6`  
		Last Modified: Tue, 30 Sep 2025 00:48:13 GMT  
		Size: 1.3 MB (1260905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eba3fdc25ddb344ab1aea9a8e50690d242abf6f211f7d36a1e90194b21ee83`  
		Last Modified: Tue, 30 Sep 2025 00:48:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425b67a7daf9d8eef3914dcb770359ac4e1315b1d895eb044514abe6e1424b3b`  
		Last Modified: Tue, 30 Sep 2025 00:48:17 GMT  
		Size: 36.5 MB (36537005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2780f824371fbaeea55a92a650900860e48db49ad8a1bd2d38abcb88e21b6`  
		Last Modified: Tue, 30 Sep 2025 00:48:14 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f9a8d549fd8ab9379dc538413a1eeee1e43d5b1fe731474774d723af7c4026`  
		Last Modified: Thu, 09 Oct 2025 17:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0124607bdd99ee296256ebbaf1e9e6ca0ab4a42d60d8cc282c82b10941658ae`  
		Last Modified: Thu, 09 Oct 2025 17:28:27 GMT  
		Size: 108.4 MB (108374913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729cb6a3cf95c500f2cde870a79e16540672d6bb0d0af7fe7b1f0ba12f28c1c5`  
		Last Modified: Thu, 09 Oct 2025 17:28:10 GMT  
		Size: 903.4 KB (903395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348af7f9398683a657ac5e703844abbd609a6c5da74acad20e146844ca6768c`  
		Last Modified: Thu, 09 Oct 2025 17:28:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b251cc15fa2281ee3481eaf3225efc2e2fa9b2df1878d6855fb8dfe727e44a`  
		Last Modified: Thu, 09 Oct 2025 17:28:10 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca27cf88483245929490bb23cda5fed0ef2d6385f661b0902b32edff833af13e`  
		Last Modified: Thu, 09 Oct 2025 17:28:11 GMT  
		Size: 3.3 MB (3250788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84f307881ca649aed2a7065a11faf61b2ed9fa243111c5a8ee5dd8d4c38e031`  
		Last Modified: Thu, 09 Oct 2025 17:28:22 GMT  
		Size: 58.3 MB (58305979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1f68a33a783387f02faa130ca557e6118071200cf2062c786fed010c19740`  
		Last Modified: Thu, 09 Oct 2025 17:28:10 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:95e8c9c7bcaf1fdd8f66757d8a80ad26b634f60197f070fdec105d0250278079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afffdfbe627467b68ee35086bb76bdfa9b347459605a3155100f948e8bcc958`

```dockerfile
```

-	Layers:
	-	`sha256:1dd917197070600c56d7f61ac33b9d9952120cee3b5cccd290aa3d84564e4465`  
		Last Modified: Thu, 09 Oct 2025 19:49:48 GMT  
		Size: 40.8 KB (40754 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; 386

```console
$ docker pull redmine@sha256:7b20bbb25fe09d92c981cd3bb5925b6edb6973cdc9e1f07b1e56ecc6e134788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240317404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd914d970cdd8462deb644f0992e7cac77dd72c9e8ba4bf9c4b0fd941bf6dc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d479fca41b7933b07d6520956ab83269dfac079d758c1dfd246463e2bec3ec35`  
		Last Modified: Tue, 30 Sep 2025 00:44:37 GMT  
		Size: 1.3 MB (1286783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9590a8fe6e7253e01db16825f4a0953165de92461fc877a7266c319b23179d9a`  
		Last Modified: Tue, 30 Sep 2025 00:44:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14a6a8d2303697fdfacf542abc7b06880575b053feb008f883207e82afb5bc6`  
		Last Modified: Tue, 30 Sep 2025 00:47:06 GMT  
		Size: 32.7 MB (32706402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d62d05a7244d2e89a7d831cd00a15dbbb8cf514b1466d6f895d5983e4f87b59`  
		Last Modified: Tue, 30 Sep 2025 00:47:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c46ee555491ded39c77f2eb3c1e2ba8db1eb8fae0895ba808a5c88b101064f`  
		Last Modified: Thu, 09 Oct 2025 17:28:21 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e92a9beadba335130fc7a8dddc82371c56985fed24ad2d216f787fe08c5cda4`  
		Last Modified: Thu, 09 Oct 2025 17:28:40 GMT  
		Size: 112.4 MB (112441864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90ac37f16d740a428deee31388fdfb186f5ae9b5ce1c875f73b7e8f9f7b34cb`  
		Last Modified: Thu, 09 Oct 2025 17:28:21 GMT  
		Size: 918.7 KB (918679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4167e0956df930d72cefd30032910d6eb351ab9c05ee26a1ed6d6a6fc5ab33ad`  
		Last Modified: Thu, 09 Oct 2025 17:28:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eae268a48e6597310a07e8d972f27d736a9db0b615972e26c6d3392e606d2d`  
		Last Modified: Thu, 09 Oct 2025 17:28:09 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726280dda64ea45a66e3d519a2881802823b0c4f8ac303fe99060f678f0977fe`  
		Last Modified: Thu, 09 Oct 2025 17:28:22 GMT  
		Size: 3.3 MB (3250793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d23a8dd764f25a3fd5ff8258053bffc80ce730934bdd3280167a8e90f81951`  
		Last Modified: Thu, 09 Oct 2025 17:28:28 GMT  
		Size: 58.4 MB (58414228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e80937da10868bb48b58489fb88b9f21df5e13013d2146281d56a3b0c9382ad`  
		Last Modified: Thu, 09 Oct 2025 17:28:21 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:75d4f044ff472a132cb74e20cb48405b8c7b37cf79fb274b1278062f7745be71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 KB (40499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd9bebbff2838c0f4c28d99ac756b4b593d7d4abe270f3eaf3ec0325f790238`

```dockerfile
```

-	Layers:
	-	`sha256:06e62d3492edef7e3ab16849e5bf68e619a1478588d395da22dcfb32f522f7f3`  
		Last Modified: Thu, 09 Oct 2025 19:49:52 GMT  
		Size: 40.5 KB (40499 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:9641d25b2db7786219d318176d69fc68770c0ce3bd5e8084e79b59490e75c7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262880558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884b911af6467346001a8873d428ee408066f30470ad1696bbb4aa0a791b5584`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0409d305744b7a525aba972827dcd4e4264d3cd0e5999e43646881651df684`  
		Last Modified: Tue, 30 Sep 2025 13:06:31 GMT  
		Size: 1.3 MB (1309672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc7731d432cef6c5a17b47c30b12ec736f3737ac4d9a4ae2ccc205b5e03cdaf`  
		Last Modified: Tue, 30 Sep 2025 13:06:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd2be62a7a89717da863cb6860c3eb4a87425177fb4798eb9d543c050ebc518`  
		Last Modified: Tue, 30 Sep 2025 13:23:05 GMT  
		Size: 34.4 MB (34397309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23eea160c7a899e251487579c995859d37097f1657186539893ebc39b089e16`  
		Last Modified: Tue, 30 Sep 2025 13:23:03 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8c6cea55e90019d2a9d2c685918c375bd4fc76b63b8819abd08060c67514a6`  
		Last Modified: Thu, 09 Oct 2025 18:17:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3065b82282f3409b35ec41c772916bd1ef9a4a408b957d85f228f3e47cf46`  
		Last Modified: Thu, 09 Oct 2025 19:50:27 GMT  
		Size: 117.4 MB (117408661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc623a43c28181a9c4d79ad6c00cc798a3611e5eed5b7db1d6932829b9f4905`  
		Last Modified: Thu, 09 Oct 2025 18:17:10 GMT  
		Size: 910.0 KB (909980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8cf6069098c6309c3cf1a2765a24b7aad89733cab6e2c68f5f528006f9bff9`  
		Last Modified: Thu, 09 Oct 2025 18:17:15 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662d36f75a790ca572ec95df89ca0aa7713f3d243b2864671546c5e3f4ac48ff`  
		Last Modified: Thu, 09 Oct 2025 18:17:19 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505655e5dff999aeb42532bf0bda870dace6002bf377beee4a9005d32e23bd4c`  
		Last Modified: Thu, 09 Oct 2025 18:17:22 GMT  
		Size: 3.3 MB (3250794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373bfe7a15f52050c99bc2a508ecf322bda79de8932b0046eb4ffac7728d1ffe`  
		Last Modified: Thu, 09 Oct 2025 19:50:33 GMT  
		Size: 72.0 MB (72001568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6122744bf91a006c7f6358bf567c151b416d54dc215bf01d1d7bb572486b564a`  
		Last Modified: Thu, 09 Oct 2025 18:18:04 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:75bb761c28023d814f82179724265cf2fb1222e7a23fc405b03f949a32659ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2901f11032857599a22a0ddf33ff0de41a37331f3317789d21be0362eeddd4f`

```dockerfile
```

-	Layers:
	-	`sha256:4d1e9ef69221a7ef19842bd9ab91c8733fd21f0d26e87eaf0fb579bcb3ddbf68`  
		Last Modified: Thu, 09 Oct 2025 19:49:55 GMT  
		Size: 40.6 KB (40617 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:23bd680cdf8acd186e90cd778bc11d6fe4a166e73d7f28ec56b99a920d075774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245817632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7ea4fb0285b40ad0ba052aa690ab5179bc2a0e269dc6cd06caf9c75c9779d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93edf2c2f238f4ac018f77311e382d63a00765309194dc5d31c092be485f0c7a`  
		Last Modified: Thu, 02 Oct 2025 07:44:05 GMT  
		Size: 3.9 MB (3861665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b97916f897d99300cbcaa72f066a9e246c8b781f754d24d6df394519e3eff91`  
		Last Modified: Thu, 02 Oct 2025 07:44:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b1502bf4d2c1397a01c5341d3d1425eff81428d772be6caa6677d8d086573c`  
		Last Modified: Thu, 02 Oct 2025 12:31:06 GMT  
		Size: 32.7 MB (32739344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a158e59511bf940e7e7452264b617c862fdf580a8aede449318344c98c2859b1`  
		Last Modified: Thu, 02 Oct 2025 12:30:58 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a521b44291ca47f2abc18251a7fa03e9bad5167433b09edc1e5f26edb2a061`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10b2cca7c37bd0ddd5019829fbed84f2df5ec50560acdf4ec9f7435da21964`  
		Last Modified: Tue, 14 Oct 2025 20:50:21 GMT  
		Size: 107.2 MB (107225060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b83ca372bfe168e454fcfdb2084abfc279aef320b6856fdffeb388c14824d8`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 896.8 KB (896833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec0b64721f9ad738c30f7502e0b9e87709899b37aa41f68bb5dd14014534508`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123ebaa401a9ff598d2803b0bd94219d8ac7d6368f27c96d24b347d015fe0c46`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d04c71b193dfc53027589d8bb11a44879518b08517a1609730a3abd12d9be2`  
		Last Modified: Tue, 14 Oct 2025 20:50:14 GMT  
		Size: 3.3 MB (3250788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c99f55ee97f6d0e0671fa6a0505c3928359a5cfb1d3fbe59ed43fc9cf0cef0`  
		Last Modified: Tue, 14 Oct 2025 20:50:19 GMT  
		Size: 69.6 MB (69564322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e662ddc34bd4e45bbc9254406c5dd36f6cdc58c3508288a8ff4853dbd5f3d41`  
		Last Modified: Tue, 14 Oct 2025 20:50:13 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:3707a6c07db62ec716235867684d8a3874f610e95736c3adae525f4d8f18a069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a1cad4e948f498e932b92f5da39f428713a58ae97267037d8acdc7257d308c`

```dockerfile
```

-	Layers:
	-	`sha256:6faf92542fb4dac85befdadd0b7f2d7b53b64297f624bf35d71fc92887f92aea`  
		Last Modified: Tue, 14 Oct 2025 22:49:34 GMT  
		Size: 40.6 KB (40617 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-trixie` - linux; s390x

```console
$ docker pull redmine@sha256:3fb629c5f3838031b1ab0c5b356048b05f37c77f45cd1a913016d16ff575181c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250449286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02b7429438c902a5520e46df8234b695e48cbd1c4ce618533fb8573a6d617d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 07 Aug 2025 19:20:07 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 07 Aug 2025 19:20:07 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Aug 2025 19:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 19:20:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 07 Aug 2025 19:20:07 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b94219bc2d3f6debe3a1214636652bb4296b7a0c6b41b51c442dbb55b247f6`  
		Last Modified: Tue, 30 Sep 2025 12:47:37 GMT  
		Size: 1.3 MB (1294331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d2a8514957d74c25bfc8f6b26ffb41866be42b94c7993401b21f8935aa8c4`  
		Last Modified: Tue, 30 Sep 2025 13:37:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1945bc87ce945b5bb62d173b54e6561640bd5e20a801c0b49f9a7c6fca1ac38`  
		Last Modified: Tue, 30 Sep 2025 19:25:00 GMT  
		Size: 34.1 MB (34067308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f887e1fd809cceeaa39ae1ad8b8041f0afbfbb53225ad030eadc7828268922b4`  
		Last Modified: Tue, 30 Sep 2025 14:01:52 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338cc75db2e74bd29c3b8bb7b3ee833378785fc31adde7c35c6cd8b0515fb3a5`  
		Last Modified: Thu, 09 Oct 2025 19:34:00 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ddc865f7942e4314f5ac1a01e498d385c061f1f61354221e70ccff2d562886`  
		Last Modified: Thu, 09 Oct 2025 22:50:09 GMT  
		Size: 110.8 MB (110760148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25793168fa57c7e317aabdee2145cfe1ffe7a97b3de8e72f50ed0fb04f87fc3`  
		Last Modified: Thu, 09 Oct 2025 19:34:01 GMT  
		Size: 922.9 KB (922887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c295c5762d6f59dc225216060f427c70287eb3af8392350ecf1513788b8b62d`  
		Last Modified: Thu, 09 Oct 2025 19:34:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cf11efc77bf4d78b98755ff222d8cde6c45b4210db5d974db032927a349bd`  
		Last Modified: Thu, 09 Oct 2025 19:34:01 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a67978182e1cb96999067a798b23b2c699d2163b1c92a366d5d48d57bb85beb`  
		Last Modified: Thu, 09 Oct 2025 19:34:02 GMT  
		Size: 3.3 MB (3250792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdcd7a39d98b8440639339f9b5e67a18e722a6cb52694d67dafa3acc38956f8`  
		Last Modified: Thu, 09 Oct 2025 19:34:07 GMT  
		Size: 70.3 MB (70312474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88ceaeb64ee8a1169b3646adbd767458533792d455dd3d83526ae32c5880d1e`  
		Last Modified: Thu, 09 Oct 2025 19:34:01 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:66cd52a09f4ea889668c73f33fbbbf75ae90b2822ee5233b7f3e341c2edaeae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259a8a8fe5eeb61b1f6d2dacffbb2406c80b5a4a45b6f8ce79fd6fab002fdc92`

```dockerfile
```

-	Layers:
	-	`sha256:31b47bee085c586c914e1148771bddafb9000227721e73e609fa9fd15eeb6cce`  
		Last Modified: Thu, 09 Oct 2025 22:49:32 GMT  
		Size: 40.6 KB (40551 bytes)  
		MIME: application/vnd.in-toto+json
