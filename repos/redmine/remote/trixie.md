## `redmine:trixie`

```console
$ docker pull redmine@sha256:c61ddd19bad3cd208dd6c210670bad73dbf11000a59ce040c70dacd6a9d4acf1
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
$ docker pull redmine@sha256:bc2f8753742aa8ceef97b2cf6cbbfdeb1ce5c5f190424539b6dc23504b41fd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258204576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecadec6c53ea9f88f2324f7cf25dedcab9fcc29747e685a85b62fdece448e41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:24d8bdec960877d7ee206d2f15c47639759b95982311051584762eb2ce240574`  
		Last Modified: Wed, 08 Oct 2025 18:13:40 GMT  
		Size: 4.2 MB (4238635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389fb9e5ae8d6da3d20eaf487829897c73321d17e1ab7e021648c8c10920373`  
		Last Modified: Wed, 08 Oct 2025 18:13:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061fb72dc7059a4a75ce34cdebf796c32a399933add82b6c2d4e6c1c38504b39`  
		Last Modified: Wed, 08 Oct 2025 18:13:43 GMT  
		Size: 42.2 MB (42158193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df15fa3f48d05688e09699861cc15024f4e69279393ac93c3c64fccf042d7ada`  
		Last Modified: Wed, 08 Oct 2025 18:13:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ee1dce5cff53b099fc5dacd65cde8d2b5965096bee4b3c6aedc448ea8ea916`  
		Last Modified: Thu, 09 Oct 2025 17:26:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def14cbdac90c3aaef789f5cd5511042efc02ad08485a1522c9f8f9c348823e7`  
		Last Modified: Thu, 09 Oct 2025 17:26:34 GMT  
		Size: 110.1 MB (110147048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f621742ce4ae1bf71a3a3e8144cbf1d041338da5370a698e7ba994713d6c59f`  
		Last Modified: Thu, 09 Oct 2025 17:26:18 GMT  
		Size: 949.9 KB (949857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d143bb23c959983709172456ade51d6f675ea76728bc0da49336f73f0e64b5c`  
		Last Modified: Thu, 09 Oct 2025 17:26:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd077bce96b33dc4c59461388d7016093b2e51807978b9b7cf194aa02d2ebfb4`  
		Last Modified: Thu, 09 Oct 2025 17:26:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0ff30f743c258bf66a9dfc40c574dcdae48d563133bedc709d670013539895`  
		Last Modified: Thu, 09 Oct 2025 17:26:19 GMT  
		Size: 4.1 MB (4139981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258507a3435d038b7d281e6c1a8f13b20cc601ec7eb3a0f5549f592b814619b`  
		Last Modified: Thu, 09 Oct 2025 17:26:30 GMT  
		Size: 66.8 MB (66788976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfb863de084b3edfed16f2924255b1dc39b0a3afe7afef6167d45ac2820438`  
		Last Modified: Thu, 09 Oct 2025 17:26:18 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:f69dfac6c98a8c6ff6898c508735ba1bf20e2fd182f359cbbebc4ee5a5a8161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa74c19b9d461b0ba906d06849a7e8f2f0a32e83ffe3ab475bfd7aa6c6d13d5`

```dockerfile
```

-	Layers:
	-	`sha256:5c4cbca92bc137f5383262ef977437c7a2be5dd3c2b8dbcf7fc6da346748f15c`  
		Last Modified: Thu, 09 Oct 2025 19:52:20 GMT  
		Size: 41.3 KB (41286 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:fc91ef0b55fe66f97aeef60634d517177d2483e18b9d35c52faeda9bb777d954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259953031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be140d855e74743db5f519d76dadd75c5f808ea5e0f80e71cedb0ae24e1d6a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:46bcf65780905045dcf3ed054acc5c607d0acf90eb8f66e81154d5753fe39803`  
		Last Modified: Tue, 21 Oct 2025 03:19:34 GMT  
		Size: 38.0 MB (37992168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3c22b548c2c045cc1122f62d8ab119ce62a999fa3057c0058e28574c519be`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8374342858be73251be33f1388352ba574a380bc5d9e9913e8c9535ac944bb02`  
		Last Modified: Tue, 21 Oct 2025 04:32:24 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0181f70aec8429544f04330dd945dced2bfbdb7e4dd4b1afa27e00aec495eb7a`  
		Last Modified: Tue, 21 Oct 2025 04:32:44 GMT  
		Size: 105.9 MB (105935809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a02dae67cc7c73f1495330f14eb0bb8d61706c4da916406d4d097cdfee430e1`  
		Last Modified: Tue, 21 Oct 2025 04:32:24 GMT  
		Size: 919.5 KB (919464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c0fa469f47a271cec2303cf157715323208e25d88a148ff5549cdb5e602311`  
		Last Modified: Tue, 21 Oct 2025 04:32:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47940562b4dc28cb5b4571b8a77d0eb5b99e19bb787feafa3156739b04385b7`  
		Last Modified: Tue, 21 Oct 2025 04:32:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e2acf38d38aacce8cc75399e5fadfb8b85ea6bc37f406636c0097dc7ccfb0f`  
		Last Modified: Tue, 21 Oct 2025 04:32:25 GMT  
		Size: 4.1 MB (4139974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e101419c843008f84551008e650c228e1855f51592799de27f642e4cfa27b8c`  
		Last Modified: Tue, 21 Oct 2025 04:32:34 GMT  
		Size: 81.8 MB (81752328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714c9a374115bef8d366b726d0b25fde0a2e716ddb47d668174cac2fe084eb1`  
		Last Modified: Tue, 21 Oct 2025 04:32:24 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:113bb4f48d623495eae6bb3507fdfecc00ec0cd12c4a943283acb01ff8fdb3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999750663529f7fa20ca9a91c1774ccbc6368ac7bccdf1ce388eb97f1fd51cfc`

```dockerfile
```

-	Layers:
	-	`sha256:76e6444d4663130c8d92ca88f124c6818dc661625aa7a315385750525547e691`  
		Last Modified: Tue, 21 Oct 2025 07:50:19 GMT  
		Size: 41.5 KB (41463 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:9b3129112f3305c06efe25df8e893ea648d14ed10ed6ccf25396dd9b2f0e7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252823242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afb3b6c39281efffadff1bf3d1053595beb596baa2398c932f4af7534a45202`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:cd3aeb9fd4096f9d44690c3294fe0e761902056d0370cd8395775551244e364f`  
		Last Modified: Tue, 21 Oct 2025 03:52:44 GMT  
		Size: 1.2 MB (1236034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7423d39587481c73ea8d56f3c00861ae144ed67312b6b83bb40e31c31b3fdda8`  
		Last Modified: Tue, 21 Oct 2025 03:52:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ae4af8941f2b4118f4bcc91b317d0be88a2118374d3c2d0373eee24a84ff33`  
		Last Modified: Tue, 21 Oct 2025 03:52:46 GMT  
		Size: 37.9 MB (37864971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73bba6271b7e6fdde1202218fe223d022c28ff2e7da4708f3dbec41a564e55`  
		Last Modified: Tue, 21 Oct 2025 03:52:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e953affab7bf6121da22f44f04e316adaf817b013096a3085292fca92d30a3a`  
		Last Modified: Tue, 21 Oct 2025 04:39:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bcfa785e9601cb0eab8bebbcb37f6f95714de00d4a607526f94407352c982f`  
		Last Modified: Tue, 21 Oct 2025 04:39:42 GMT  
		Size: 100.8 MB (100842523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c7a451c9d110a893e523c23336ba3736a0f15a852799beccb0255aa8ec5252`  
		Last Modified: Tue, 21 Oct 2025 04:39:34 GMT  
		Size: 915.3 KB (915258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488d4b1598330637c22ebe3a0701a3ff26d8925d574f64e8089e632c12a88000`  
		Last Modified: Tue, 21 Oct 2025 04:39:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a764313b61db3afe31180cd41c6b23db43525c52be2ee96f6734818a45ce0c28`  
		Last Modified: Tue, 21 Oct 2025 04:39:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798c16fed4883458f769faedd37a61b71f61e3e5adc5c6b06f8d01374d4a18d9`  
		Last Modified: Tue, 21 Oct 2025 04:39:35 GMT  
		Size: 4.1 MB (4139974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc560e56053d7f61cb5437943a9548b3561f9ac9e57b35d71951ae14aa4253f`  
		Last Modified: Tue, 21 Oct 2025 04:39:40 GMT  
		Size: 81.6 MB (81607474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fe33d6832d3f61bc64782c54fcf4871475792032bffa92285d736b6913dec`  
		Last Modified: Tue, 21 Oct 2025 04:39:34 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:b210f7af1a61a25cae039e67fc80093287d466b4edabfac3f56030c154607a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e3319b863f430ac88dff1aae9b4db07369f632dac12d350f7e4436f10bde39`

```dockerfile
```

-	Layers:
	-	`sha256:67dcc70957b02ccb31d787e5c0bda9021830742c9e6a63cd6ea94504c6413cc4`  
		Last Modified: Tue, 21 Oct 2025 07:50:22 GMT  
		Size: 41.5 KB (41462 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:8363e1936636ace7c917a3b507f46a4db954ecfd3160fa1b01e18072c60df90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257197538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296ca24652f63512b08a8fea31c2ab594c80e9bae5ce7314642516b0ed22384a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:26395651123655cda4d802c26b1f8140476e16d1a677f793c94e46e9a2c4e816`  
		Last Modified: Wed, 08 Oct 2025 18:15:06 GMT  
		Size: 4.6 MB (4580398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebb7a9b5663ddefd8c81f14096634fc1f6335f6ceabab4ca5ef85ba31b1e8b`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56190edec78a7b72ae72a5b588f64dabe3fbad052613aaaf6e5a3d593a585a96`  
		Last Modified: Wed, 08 Oct 2025 18:15:08 GMT  
		Size: 42.1 MB (42145937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721e4c3729e66b852532b035ea342e7c27d33ec65788d08f5f0321083932146e`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb3b892c71ad2c0816d5ea7923349d50918d3996944eb1fad0cd3573c0cdd54`  
		Last Modified: Thu, 09 Oct 2025 17:27:10 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b143c5fd6f8e2386f16e7b6f69ae5bd86cab6f01c1fbeaf4cbe80f8e95c32930`  
		Last Modified: Thu, 09 Oct 2025 17:27:28 GMT  
		Size: 108.6 MB (108556595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411b1ed8c808a805d6586773bd018d32373396900f78070b678228f90c0c848c`  
		Last Modified: Thu, 09 Oct 2025 17:27:10 GMT  
		Size: 903.4 KB (903363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d320646dc02ad645079fa6609a1cbd0a3c26663fdb353933d0a881476c45ba56`  
		Last Modified: Thu, 09 Oct 2025 17:27:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b73ade8327171d3827a83564f477937e6f88835c5b2c1705895e99a913e34d2`  
		Last Modified: Thu, 09 Oct 2025 17:27:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871c46b38a4ef1f80c0c6640693bf3a66d084349d7887c03d2448bd746cd28b`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 4.1 MB (4139981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf97ffb4804251084672384ada85d8d8651c63feacfb0279f925a83a064e414a`  
		Last Modified: Thu, 09 Oct 2025 17:27:16 GMT  
		Size: 66.7 MB (66726300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6060729b6d3f4a9fcb8b5d25cb92f8a36193c30232b0b376aa3643cffc9fd1e6`  
		Last Modified: Thu, 09 Oct 2025 17:35:25 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:7e64d509b24ac704224a6b0fbbefdaae7a6dcecec8b4ef42429b1fa285397bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211dfd357239e171c23d181f46e96248c247a1d474a784308019f7f38741b75a`

```dockerfile
```

-	Layers:
	-	`sha256:86efaf883ef3a44f869e28d7b6dfeaffc2d9c63794aaec35695d8c78aa0316a8`  
		Last Modified: Thu, 09 Oct 2025 19:52:30 GMT  
		Size: 41.5 KB (41513 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; 386

```console
$ docker pull redmine@sha256:f7f99366ec5f7b2991fcf1f94d924e8c4e966596e54f48f79b10d88dd7ecbf3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275032311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e22d357b6b2d70e7a129de176228c22813d1d504bdfe3966ffa39b8dc6d41d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:c38853ce4b0e208a9125060e0f456e14b3a9ab585922967532c7d59b6f77e5ab`  
		Last Modified: Wed, 08 Oct 2025 18:13:04 GMT  
		Size: 4.2 MB (4176773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40a40417e96c0bf31059a28f05b62d7bbadffc1a9c5608fdab6cf1affc135bf`  
		Last Modified: Wed, 08 Oct 2025 18:13:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6e211ff62ae87d57611cf475eab5282adc23aa930f995a3f33476752fde394`  
		Last Modified: Wed, 08 Oct 2025 18:13:07 GMT  
		Size: 37.7 MB (37739616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52cb76b74cd5407c97bd9eaab20872f3dc3166eaf3d57a7139a921f390d2c67`  
		Last Modified: Wed, 08 Oct 2025 18:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bfdbd871a9bede098e1b666713c12efde5e9c2646c67ec12c023e02d98b583`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341ffeb5dc4895128f31add9e3c70be6fc3fc73cfd01080f38d1eef2ae505f2`  
		Last Modified: Thu, 09 Oct 2025 17:27:20 GMT  
		Size: 112.7 MB (112657496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe75b12f5965c98e87d9d115c02ffdcc2fb17aa6ac18a87712c7027641c1837`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 918.7 KB (918675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c9ed2ae9d1f657d977ee55bf281f757b9805816ea7d8167b2ab190db63b994`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1136c5d54850ce117490197449e7122b821f85d02e4ea4374d48b4cbe79ffa5c`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d7a5618d90c3de785dad9026f04709801a0615b9b0e8ff990b309d06cd4166`  
		Last Modified: Thu, 09 Oct 2025 17:27:10 GMT  
		Size: 4.1 MB (4139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b8b53d76109705c69c93e0dc73e32a489c133132c8a968fe6374946652bae`  
		Last Modified: Thu, 09 Oct 2025 17:27:18 GMT  
		Size: 84.1 MB (84101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df46e909ad00b68c3f3b6c213c98c61e1f52d42149bda6be4986068e8e0ef94`  
		Last Modified: Thu, 09 Oct 2025 17:27:08 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:abb944195febe403dd69e672d291c7a6838906d23d64247b4b3e8ac269f9ac1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb896365acc367de269867f1e9b5cf6ba766f07939f08ae305bcba90c6dd39d`

```dockerfile
```

-	Layers:
	-	`sha256:30f404ed5944dd3473de691b2d398faf7dbcc12581dc48cafc5e9ed9374b058b`  
		Last Modified: Thu, 09 Oct 2025 19:52:33 GMT  
		Size: 41.2 KB (41224 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:86bfba89bb523c574058d3fe25897938fbf0739ba416c8ec110ce38264a15fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298821799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47277c31b11c05ca4f882678669521111139d6cbd67c5ed39a545999b3a18600`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:976752e1a563808e28225cd60d92e3bb6790e9808867767172b4309121eaa4de`  
		Last Modified: Wed, 08 Oct 2025 18:34:11 GMT  
		Size: 4.5 MB (4506224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cea3fea55897793de99e882604e5227f8d308b3611254944e0978b42fd0a02`  
		Last Modified: Wed, 08 Oct 2025 18:34:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dddee654d8a14423bf04021346233f1ec931d1be3befe7b74e9ef5c007d3552`  
		Last Modified: Wed, 08 Oct 2025 18:34:20 GMT  
		Size: 39.6 MB (39601279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d2a15cb239e606145ae050249a588d0a1de8632500feda3544978ed17e975e`  
		Last Modified: Wed, 08 Oct 2025 18:34:09 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1b1cc931506ce5da89289476e4c10c0695827c6b9ce556ae4fd1145ea6413`  
		Last Modified: Thu, 09 Oct 2025 17:30:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35356ffb42119a01bf1b1d4b60aecb74444b8ab4a0654bd0ae129e60905542b0`  
		Last Modified: Thu, 09 Oct 2025 17:30:28 GMT  
		Size: 117.6 MB (117622692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab28c816d23368a5b93f331268e22a47bd2f1db8310b5231a7ec29828a5128d`  
		Last Modified: Thu, 09 Oct 2025 17:30:10 GMT  
		Size: 909.2 KB (909200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb67ab3566397a9705b37c35a38556467593f350a8f8e374ff41d9aaac298e3`  
		Last Modified: Thu, 09 Oct 2025 17:30:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c737ffb926868e3e4b56eaaa9ffe090c03d0489a1e5b0069ed075ac32beed9`  
		Last Modified: Thu, 09 Oct 2025 17:30:10 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f76e4875ba842f1e074d998dd3e5266d64f60862a069d88c16c7c3d4099828`  
		Last Modified: Thu, 09 Oct 2025 17:30:11 GMT  
		Size: 4.1 MB (4139981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547e2ffeb23c8d4c1040e1d5a28fb0cb1d6636e8d11c6321d5a856abdcbd29e1`  
		Last Modified: Thu, 09 Oct 2025 17:30:30 GMT  
		Size: 98.4 MB (98439846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc700f2fe79890b07e4aad3118c81ea65f3c948b73b069757498513af19fd8d`  
		Last Modified: Thu, 09 Oct 2025 17:30:10 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:6eb9c9b0f0849acec1b3bb599023253a24410bbd9ad0878cc3dcb34cab47e44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44ea1ec139ade783ca67d4c11a9ada84709d203c31181ca654f228ac8867a8f`

```dockerfile
```

-	Layers:
	-	`sha256:6ba8d82655d79a5fd43373df56362721f1668c520dd4b383b7ee866412ff0c69`  
		Last Modified: Thu, 09 Oct 2025 19:52:36 GMT  
		Size: 41.4 KB (41363 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:d10baf3f56d415112ad726559b4f39a49c57f69304cad3d4cd09c632ca825620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282165640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d3631cf6862fbd2a65ddaa9a769f358ede3c86d19c14badc7c1a04cb4381b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:17cb807284daad75c5fa3695fef1d2d37861b8908199bc341ce4ea3d64611987`  
		Last Modified: Thu, 09 Oct 2025 00:41:45 GMT  
		Size: 3.9 MB (3861785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7712b4b26af05218185cf0ac46549fb825a44232f2916383d5dd7583ade75c66`  
		Last Modified: Thu, 09 Oct 2025 00:41:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bca0a2d50507123a93ca8c134e3c84d998f76a509095be909ddfbbe2c205a`  
		Last Modified: Thu, 09 Oct 2025 00:41:47 GMT  
		Size: 38.0 MB (38001485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf0232d6ce42f4796dbff677980604031cd8427b2c75a100c1593097164bfb`  
		Last Modified: Thu, 09 Oct 2025 00:41:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7f846dce16a57ac776536f3fbf502052bed145e5d77c42c0d8d5697086e8e`  
		Last Modified: Tue, 14 Oct 2025 15:03:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb985e5e109a38c5ed49000b702ae3de17b7ba30cf30fb8a12c46e2cdaa3f41`  
		Last Modified: Tue, 14 Oct 2025 15:03:19 GMT  
		Size: 107.4 MB (107394559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beac682c517e514c931fc7e332c7024d137de770b31d986028fe00b6df8d7ae`  
		Last Modified: Tue, 14 Oct 2025 15:03:11 GMT  
		Size: 896.5 KB (896513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9069a8a7f4b671174806b9149b6a30b7fd395c1c58798676856636a267f6a3bc`  
		Last Modified: Tue, 14 Oct 2025 15:03:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ed5646d95c0775638a3ad398f6e3739119c22743d34b5ef90ada899cc10cf`  
		Last Modified: Tue, 14 Oct 2025 15:03:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c006c9d623b5367f5eb499f449c4888012abd8f0d5fc6eac3f6469f84c2a91`  
		Last Modified: Tue, 14 Oct 2025 15:03:13 GMT  
		Size: 4.1 MB (4139986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6b4c8518162bc72028ac0ff3be3d9b9e1df5578c68fc61c239be1da355a514`  
		Last Modified: Tue, 14 Oct 2025 15:03:19 GMT  
		Size: 99.6 MB (99591689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c7f8c235cf7ecc83914c35de7c3876fa2d1ff6413c3bae23fa521c4ff8426e`  
		Last Modified: Tue, 14 Oct 2025 15:03:11 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:7acef661ca5d36c835e78fc6995d1f1e1b8e78e94cf0fa90f04b0d1d16cc2f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aed4035c5a77bbcd900441769136a469cc675ab6a113899f313b2fb91e352af`

```dockerfile
```

-	Layers:
	-	`sha256:65d41d347810bef509bbc53ba8b82ba0245ae3dc05bf2d008562a183df37ffb1`  
		Last Modified: Tue, 14 Oct 2025 16:49:57 GMT  
		Size: 41.4 KB (41364 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; s390x

```console
$ docker pull redmine@sha256:56c3421c5f76288498399cf488128f69f2eac3cc63dd8fb1d383a77a8e47debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286552238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe00d20f0c0b28a384c71e8bc57271cbeebdc8fac5a12c2c7eb20fe842b7fb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
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
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:f643f8d7858021a97f0967638ee5bcabf0d4351b2c38b20664203c2db9bf4681`  
		Last Modified: Wed, 08 Oct 2025 19:10:59 GMT  
		Size: 42.4 MB (42365078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec945648ffcc1fed2409183ddc544cf232ac1c087af685ff7ee54c6060b972d`  
		Last Modified: Wed, 08 Oct 2025 18:23:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30005fa999beaeee072d95ec6500c015c4ed97d1b91cb288bfa1c8e87334428`  
		Last Modified: Thu, 09 Oct 2025 19:02:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1b027d6e458a9d67fe3633ae0ba78be3250b277cc957eaf86af869a60b66fe`  
		Last Modified: Thu, 09 Oct 2025 19:02:06 GMT  
		Size: 110.9 MB (110945647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9922d171baf57c6857b33142225fb39bb35b259fb85c2e9e98942699a970b2c6`  
		Last Modified: Thu, 09 Oct 2025 19:02:00 GMT  
		Size: 922.6 KB (922623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf03e40da5bb7406a80b37e0d6caee702363b8ec8e0ecd77c83a4ad53016376`  
		Last Modified: Thu, 09 Oct 2025 19:02:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857826744138014e56859c60883c0cd21c84ba8aaca36176433d00e58f2f0e52`  
		Last Modified: Thu, 09 Oct 2025 19:02:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe692ff945ffb9c463bf86c0acd33c58021a1096910e93ffc7e64091755ea0a1`  
		Last Modified: Thu, 09 Oct 2025 19:02:00 GMT  
		Size: 4.1 MB (4139980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fcfa8234596bd9413aa46705b4b79995f85ee0c5bd22a837087a798912c802`  
		Last Modified: Thu, 09 Oct 2025 19:02:08 GMT  
		Size: 97.0 MB (97043229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797d08e25bdc05c1bad074feabc635109907a8daf9d4ac22d0da138fabc83b1`  
		Last Modified: Thu, 09 Oct 2025 19:02:00 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:542f6ce88d914d1516ae3994f769aba8278fb7da3e09b9cb799bdd8890bea56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e38c9f6f4be0011046f534d88687249825900d8a55135165841e441a4a6ec3`

```dockerfile
```

-	Layers:
	-	`sha256:832da84fde526c28ef013f70e65c0948db57b8d288d159e2d8b0d333b1008a6a`  
		Last Modified: Thu, 09 Oct 2025 19:52:43 GMT  
		Size: 41.3 KB (41286 bytes)  
		MIME: application/vnd.in-toto+json
