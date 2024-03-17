## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:7ce83c55659ae3697c53bf75ac4b4b0a338a1588dee40a204a8e51541e44b90d
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

### `redmine:5-bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:855e66f18c59532712b7f835407eab3ea995656e2a154ed7a7969a5ec982a664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258628675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc31f23f47b1e859f6d3054d6870797f20b87d0713999a1bbc5c3ed2cc4c345e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9479953a16c727f19abaa10d54d91912b9f91434239a10dba5481a2414e3dd8d`  
		Last Modified: Tue, 12 Mar 2024 01:59:41 GMT  
		Size: 13.8 MB (13848702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0cd6abf629614451709ed38fb6c3924d5c1de83c612a959387ee890c0f50fe`  
		Last Modified: Tue, 12 Mar 2024 01:59:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb5e8a75d344ec58cb501ca2b6b83f3548cfe807c5f288a63c27f06cbc15750`  
		Last Modified: Tue, 12 Mar 2024 01:59:41 GMT  
		Size: 34.8 MB (34816686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ddf37a49ae28d721bb67e4f4c550f5bd54579226eea7eb2c7e4e6c9298cd67`  
		Last Modified: Tue, 12 Mar 2024 01:59:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5742bb6542957659737b7476f14034632ab50793c0c9b0d5486a520b9dd0e3`  
		Last Modified: Tue, 12 Mar 2024 02:56:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83767c2586608d2da875bebdf6dbfcd8297cbea5508862e7af712a2c1b502644`  
		Last Modified: Tue, 12 Mar 2024 02:56:50 GMT  
		Size: 122.2 MB (122150047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb04cdc82f6ae0e0880df3c3165b6edf3cdc159a1a95be7ca41efac6c288e16`  
		Last Modified: Tue, 12 Mar 2024 02:56:48 GMT  
		Size: 1.2 MB (1152887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f6c5eb2ac3291a7ab304b48ee68fefacf59cc1615e4c31bbe200e1b1feeb66`  
		Last Modified: Tue, 12 Mar 2024 02:56:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8610b6500e58f65e455be4cfcfd5d04530794e44485d2699c4dc9946d2e796e`  
		Last Modified: Tue, 12 Mar 2024 02:56:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a445d3d648360e8901922825a360f5c3c00433ad7792ab5bef392390443913dd`  
		Last Modified: Tue, 12 Mar 2024 02:56:49 GMT  
		Size: 3.2 MB (3240633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5519d2178ef4b37f20ab3051993f578a6bacfb42764d405dc035fa5e92d4ba2`  
		Last Modified: Tue, 12 Mar 2024 02:56:50 GMT  
		Size: 54.3 MB (54291816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb3ecef83a3636f3c467f65659d152253d0fedf23110a82556ef342783e679`  
		Last Modified: Tue, 12 Mar 2024 02:56:49 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:ce6ba0f363831430f763fc6d3c9dcdb64c2d290a4c644a8f7eaaf4f1550bdc7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8900581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541dbff0f56818346c808400bd10ba94096c80e0f860be3ba71e6d7c167e8340`

```dockerfile
```

-	Layers:
	-	`sha256:437b226cd4cb0b3cd6ad6f21e0d651aa04e49997f3df46c6d7e731ef36852b4a`  
		Last Modified: Tue, 12 Mar 2024 02:56:48 GMT  
		Size: 8.9 MB (8857712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00ff54989dfd381996c9a36bba925d945d0da62e43e71bb066dfb36616b68372`  
		Last Modified: Tue, 12 Mar 2024 02:56:47 GMT  
		Size: 42.9 KB (42869 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:3a55513ce10cee4b6b74c8cdb55fd148cb43318aefb25021a9215cc6c269ef98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240962819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b078382efcad85aceeba02895c375a68f55e10c9e176cc53af78a9bdfbee6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3cab369866146ab2f84a0f073289eadc49bb7055578603cc1d299a26c6fa74`  
		Last Modified: Tue, 12 Mar 2024 21:23:52 GMT  
		Size: 11.6 MB (11606541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd6e2c5ab60ca3bae132813b19db922494eed41fe397ce303eae2d91e026173`  
		Last Modified: Tue, 12 Mar 2024 21:23:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6427b3ae23f4435f46372d97badd4a84118983d65617afdf284e9b10624fb29c`  
		Last Modified: Tue, 12 Mar 2024 21:45:41 GMT  
		Size: 30.9 MB (30905745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2456b032420223f191afe7c24ad0f73d8f689e8560afe93d422db2522f7fc193`  
		Last Modified: Tue, 12 Mar 2024 21:45:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b430c1a06b94f3863a840a7e57f67954a8cc84756a7c275553f6a48929c3`  
		Last Modified: Tue, 12 Mar 2024 22:54:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7096a1f21b03729d347b2dec306154474a2dcc30c20e350483d0a17c8937a8`  
		Last Modified: Tue, 12 Mar 2024 22:54:07 GMT  
		Size: 115.7 MB (115671925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479965c2e1a6eb5bcf5980b72a27095c386ed4f607afb26c0e5c1f96ecf634eb`  
		Last Modified: Tue, 12 Mar 2024 22:54:04 GMT  
		Size: 1.1 MB (1129595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167257c32feb1e99240eca0c81cc5414b4ef57d771a40fff56dcbcae0c248916`  
		Last Modified: Tue, 12 Mar 2024 22:54:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91804d27fb3c66055c3388b006739874356c55651bda996f1655f2d0e50fe646`  
		Last Modified: Tue, 12 Mar 2024 22:54:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbafd260818ef7f3bbc222d1aaf8b9cca861dc82733021c6e411e7401bd71ad5`  
		Last Modified: Tue, 12 Mar 2024 22:54:06 GMT  
		Size: 3.2 MB (3240634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0ce585d98408d4eb99d0a6c0f7c3ace4748b9723d1db0b8261382456b9c5c`  
		Last Modified: Tue, 12 Mar 2024 22:54:07 GMT  
		Size: 51.5 MB (51520632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bd964657f47fb866e099e407d419ced91ee4ed26e142f13dd4a3d3ba8a00f4`  
		Last Modified: Tue, 12 Mar 2024 22:54:06 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:05f54a74d7826513f08906b7448e961ae6687603af08eaf5e9d6eddb1895d7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8864625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c86cd251924b0a3c0071205aa77186a3bcab530dc147e72160042d15eee0502`

```dockerfile
```

-	Layers:
	-	`sha256:eaafe4e1d1cedde583819da7e67812fe03d188acbd88f525c13a6d258d1c01ff`  
		Last Modified: Tue, 12 Mar 2024 22:54:04 GMT  
		Size: 8.8 MB (8821524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410e130a689122af18c4e66139573c4d638f91102eeec0b3c8e5582bdb596c29`  
		Last Modified: Tue, 12 Mar 2024 22:54:03 GMT  
		Size: 43.1 KB (43101 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:6d9c27f9ddb4faa7737f7f4c75db31f620f02131656ab87f6345e303194058f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233293822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143ea5b299c2171fdcb3d442a0f851410e2c357f06dffc50e8a6dc2d8fa9041d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc68c0f8997973466f17bb8a21d258cda94623205259797a08c5939d71783a`  
		Last Modified: Wed, 13 Mar 2024 08:31:16 GMT  
		Size: 10.9 MB (10943938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a50a9e00509877792156e85a18c335dcbc277b943728ff38a012d2ef37a17`  
		Last Modified: Wed, 13 Mar 2024 08:31:15 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c02b12ff825c0a8ddd1ae82202b2c40e433ac943bcbe10beaf7db2848e3930`  
		Last Modified: Wed, 13 Mar 2024 08:42:09 GMT  
		Size: 30.7 MB (30740898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323092ef785df09e190f44b8b0f0e69c47b2356f7b38fafc722f64692885cd1`  
		Last Modified: Wed, 13 Mar 2024 08:42:08 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13bd68da4abf19b6c62d909778e25faf039e00f19c9f865f3876fc720e574c`  
		Last Modified: Wed, 13 Mar 2024 10:51:38 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b6219f3686923271ef010f49407d6174efbc4031ff07513097179d244e63e4`  
		Last Modified: Wed, 13 Mar 2024 10:51:42 GMT  
		Size: 111.2 MB (111160600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5c768d655d7092cec5e0bf2c33f7a313092bfe95c8447f5c98d4e95fea352`  
		Last Modified: Wed, 13 Mar 2024 10:51:39 GMT  
		Size: 1.1 MB (1118993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c876f7d8f40faff1a55fa35b87b0a7ab0a7972d35b529615f3e3793b094cc`  
		Last Modified: Wed, 13 Mar 2024 10:51:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b7b93d403c62f3ceb05fc7c8b2b0b992a9f290c14a02212c61b3ac8bec6f39`  
		Last Modified: Wed, 13 Mar 2024 10:51:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b28cf5e51d0e5b375633aa910dba895bc8ed2bd3690fde852e039bdb7d7fc7f`  
		Last Modified: Wed, 13 Mar 2024 10:51:40 GMT  
		Size: 3.2 MB (3240636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a3f702fe3e75463a624754d90fe5c0a057c51422f255dd2f3299bd84a177be`  
		Last Modified: Wed, 13 Mar 2024 10:51:42 GMT  
		Size: 51.4 MB (51368305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0026aed200d2a2811e0e8b1071104690026364f88472fa1b0d8e8270fcb6e87f`  
		Last Modified: Wed, 13 Mar 2024 10:51:40 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:4661990656644cd8bc00ec88529f966e3bd88576290fc83cd56595dd1df350d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8866046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46437d5a6e06e005f3e6ab68914d836b18b8e7eeb56d302af9aab682f2b1674e`

```dockerfile
```

-	Layers:
	-	`sha256:46952368a31db8c6c3799da157de67c7b04132d4b70f194a017ab93a5bc551c2`  
		Last Modified: Wed, 13 Mar 2024 10:51:39 GMT  
		Size: 8.8 MB (8822944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992ca7adfab0611a09e3860123d69fb4be34765d0795f42a69b9c34df48554a8`  
		Last Modified: Wed, 13 Mar 2024 10:51:38 GMT  
		Size: 43.1 KB (43102 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:05d1f2cdb10e2f6e89b67b5193fcc5d03e6c6a70fda3299c23f4589ce2b89f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253995756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3345d3e4397c605073fb0fa71e43ed2c64d372f1ebc2a056afd2ac21a52f383`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6bd85b42bd4094b4fbbbd2b116f30a765723c152936b569cb705a31d1e2c0`  
		Last Modified: Wed, 13 Mar 2024 04:34:58 GMT  
		Size: 12.7 MB (12689798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff3fae641b6e37b902bb6733b709fe0d96ac27398f625174d054358341c0b36`  
		Last Modified: Wed, 13 Mar 2024 04:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175411d8e298668e2a8e5ef63e407013d0efb5ccbe9dccc1d4ae2138332863d8`  
		Last Modified: Wed, 13 Mar 2024 04:55:29 GMT  
		Size: 34.8 MB (34780621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2647be0c1c25cf86976af37723980090446f0f6471bcb291469f6057a38da190`  
		Last Modified: Wed, 13 Mar 2024 04:55:28 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2f249d5690e9ab3e0afaa3b9bfd23598b5833f8b3e8375c817b0c5966b42b`  
		Last Modified: Wed, 13 Mar 2024 08:58:28 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62422cd13c3ffb18ac4b10d4c0d73e409f40e3c5f6a548e5d4a32d9f12ff40a`  
		Last Modified: Wed, 13 Mar 2024 08:58:31 GMT  
		Size: 119.3 MB (119348389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8933a73ca0d315c900862bad4d826c1ca838e3b797d68c7d8181576ed1b5a6`  
		Last Modified: Wed, 13 Mar 2024 08:58:28 GMT  
		Size: 1.1 MB (1084249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8dc378e07d9bc683530f764d27aa0878ef5e90d3fd29a860dd66267d993528`  
		Last Modified: Wed, 13 Mar 2024 08:58:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54cd7dd71ac57196ae24b59e841f28aa9a9f8245a2df2bddde4862cc5a5ddae`  
		Last Modified: Wed, 13 Mar 2024 08:58:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfae45bd11c018e77fd0db9f7e1204292390c0609bf2e116d32da40a2dc3130f`  
		Last Modified: Wed, 13 Mar 2024 08:58:30 GMT  
		Size: 3.2 MB (3240636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c4539c3af71712be9b2ce56fb9f6d43de848d1218b1774c1da62611733dd9f`  
		Last Modified: Wed, 13 Mar 2024 08:58:31 GMT  
		Size: 53.7 MB (53691904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693af9a9c9db8d179df2db643e256ee0303ad4cba149c30762e728ce2927f48f`  
		Last Modified: Wed, 13 Mar 2024 08:58:30 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:dc666b745bff68195cb3dd321bfdfb778a398f359961757b44c8c04af6edc6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8878330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f18a9451d1397bc0b8763343c97a5c37005240543afcd60e8db1298b917dd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ad8b1145b29444a32ac8ab97b22c3a9834796ec08dac6706539bfa7638db4668`  
		Last Modified: Wed, 13 Mar 2024 08:58:28 GMT  
		Size: 8.8 MB (8835378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17cc33bc1e53f9a8aea945beccce406928acadbd3f3b534eff8a8c974d12d3ba`  
		Last Modified: Wed, 13 Mar 2024 08:58:28 GMT  
		Size: 43.0 KB (42952 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:ce15023c5500b3f7a2974b5c7988239a5f684d966a74c3b8e3ff7252f39ca44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257585698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f041131e00e12698d8e970398fa2e3e387b35f8c4b36c353414611b19a2fe2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c34329e75ba81015d20f1ed9812aee278e6191574b344f1b224e9b3f23a1c`  
		Last Modified: Tue, 12 Mar 2024 01:59:31 GMT  
		Size: 13.4 MB (13396898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb9659d64c2fddcf168f54498e60935cfa23db4a7a0d44c8f4c612c1939a8c`  
		Last Modified: Tue, 12 Mar 2024 01:59:31 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5349b367420e23cf8a07fb84a5443b49ab739668648e923d98a07e582c6a0ab`  
		Last Modified: Tue, 12 Mar 2024 01:59:32 GMT  
		Size: 30.7 MB (30737240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4bd68496a1a6efad57fb9e9164aeae9b3a2bd30d1bd5550de851e903bd1db`  
		Last Modified: Tue, 12 Mar 2024 01:59:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb9f0689f9d4ae856cd29bdc2e9d2c21c1df955a47e515f449d9261eb4a567`  
		Last Modified: Tue, 12 Mar 2024 02:57:00 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517e1929ad932dcd854a117394459885b96888c2f6f582b5253b4e88928f3bd`  
		Last Modified: Tue, 12 Mar 2024 02:57:04 GMT  
		Size: 124.0 MB (124011419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49ce758de99c1a0aeb6561ed97f4b6014186d06535afef746097759f084e989`  
		Last Modified: Tue, 12 Mar 2024 02:57:01 GMT  
		Size: 1.1 MB (1126318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2073f5224a576ab5dbfba86cf4e0ccfabd4c7f20a2f589c5537c64b05c4a54`  
		Last Modified: Tue, 12 Mar 2024 02:57:00 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e93156ea396f692fd358d7632bd0e045347844e0fd1a103ffdf7167fea8ab3`  
		Last Modified: Tue, 12 Mar 2024 02:57:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e329aba5acc2b95b241eff912133e84f33530c86c0860def6f5d96722a31bfc`  
		Last Modified: Tue, 12 Mar 2024 02:57:02 GMT  
		Size: 3.2 MB (3240619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc6aa3fdcee3579b88fe7fe93b24a4b568bc3ba744eba9ad56af78caf197bf`  
		Last Modified: Tue, 12 Mar 2024 02:57:04 GMT  
		Size: 54.9 MB (54927610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a685544f2e44aa1c4dfd4c5fd37ca40ce49306dd33e82c79b6c410c6a68014f5`  
		Last Modified: Tue, 12 Mar 2024 02:57:02 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:483c8c6a2e0c97bce35e2688050ae81f3a88149a76c6ac617b1aaa7caa669e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8892625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88810ea1b9efe9a9a379326f4add6060131705e4f19e3c6c64d41a943eff4be6`

```dockerfile
```

-	Layers:
	-	`sha256:38f2e8d64cc1b27f3870c82857abc0fbcba9c2579ba2b3df501c8b57859c8bc0`  
		Last Modified: Tue, 12 Mar 2024 02:57:01 GMT  
		Size: 8.8 MB (8849819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919a3a96b9b83095d5e7f9f4f2fd69a51f682c32d81797b689e1d574ce94982e`  
		Last Modified: Tue, 12 Mar 2024 02:57:00 GMT  
		Size: 42.8 KB (42806 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:9db16d7f0c6846a892c5896b4364cffb43864180d6d9d5aec74e247453652720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261445673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac8a0718b7b2ac7a56030b32f239e0281be5c4eed03c2f99e7c23721e39883`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea992ad62a16bf77766e11616b296c93b913edd2abf5c1354b69dfc432c000eb`  
		Last Modified: Thu, 14 Mar 2024 04:17:00 GMT  
		Size: 12.9 MB (12871277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b42f1bf781691a317e662a1abc96b40a47bab40c82b1666167b2e2e9efe2d9`  
		Last Modified: Thu, 14 Mar 2024 04:16:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eff83c8c0e4b6f5db7dfa59c35b9c33986efb6fae840a4f9c6b0322351970`  
		Last Modified: Thu, 14 Mar 2024 05:12:35 GMT  
		Size: 31.8 MB (31774986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ccf0b053b84872aeb9360d4ee264f5b0238b16d78ce67b21590999c53ef3a7`  
		Last Modified: Thu, 14 Mar 2024 05:12:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6530ae01986d373f03f6055b2cfe469861c3c08f13f98cf01695e022f6334619`  
		Last Modified: Thu, 14 Mar 2024 08:59:35 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17528eb7821e0c38ada54cdcf2f25dc06876c8cab8cea2e0e9371e3f9202d94`  
		Last Modified: Thu, 14 Mar 2024 08:59:47 GMT  
		Size: 117.6 MB (117616098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b280faf02eacce5b2283a0e17c06583dfb78d699339e35581d214e60ed285bf`  
		Last Modified: Thu, 14 Mar 2024 08:59:36 GMT  
		Size: 1.0 MB (1039935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3337145960c5c39dd44543b7a67be8a86b8604f87e98065748bb1a5fa49c6ec`  
		Last Modified: Thu, 14 Mar 2024 08:59:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7aec57f1ab9aaf51a551e16fe3e47c7c3487bcc8cc47b1559ad5e16569271d`  
		Last Modified: Thu, 14 Mar 2024 08:59:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68efdc8aa2107f3e28d7624a839fb21d39692a08609670138c0f46fd335434bd`  
		Last Modified: Thu, 14 Mar 2024 08:59:38 GMT  
		Size: 3.2 MB (3240655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86a61027073347576ec807f1a2d30f890e221ec534ae3a5dc89d7d48a191c4`  
		Last Modified: Thu, 14 Mar 2024 08:59:44 GMT  
		Size: 65.8 MB (65779786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced7bbbf78f0b64a530f0d1163d69ba33e552a3edadf2eb0bf4fc4a5cb934c4`  
		Last Modified: Thu, 14 Mar 2024 08:59:38 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:2f4c1cde655e595cbdd6f2932fef44988fb38874fc2f7db871bb17fd5dbf69ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 KB (42830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da45601af19777acca400a8e12f9a4961ad9ed3ffa23ad18c294abcb80a6c624`

```dockerfile
```

-	Layers:
	-	`sha256:38751e02dd305c5ff28a99098b179142d05ad0683abf1ce934bf857997a53790`  
		Last Modified: Thu, 14 Mar 2024 08:59:35 GMT  
		Size: 42.8 KB (42830 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:2567ffaf23e84490f8f9da3f2b16eb27ad794ae88bdbc8fe2e4b18f71b7a1554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279845878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d936f63574ddac9a432fcca7df4d08c42f8e57bfaf8cfdff5995dae39b1196f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec39b24128124150a999dafc3a1a81a44aa7bbd28a482284ffabe39db6d1c71`  
		Last Modified: Wed, 13 Mar 2024 06:51:11 GMT  
		Size: 14.6 MB (14569793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ab8ff4dac5fbf32e172e66a3eb2196218c75360211eca353257b1192c5382f`  
		Last Modified: Wed, 13 Mar 2024 06:51:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dce54de454bb15f9c32b76fd3dd361ff07957dcc8a1764724625ed44c83b67a`  
		Last Modified: Wed, 13 Mar 2024 07:26:33 GMT  
		Size: 32.3 MB (32266612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72339d940c1778a13ab6c4366eb62c92af92571ca454c8b6851d6639bf6ea0ef`  
		Last Modified: Wed, 13 Mar 2024 07:26:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d155610391bcd0d81be63ede69aa2ce0c86c875f4fdfa8a2156f4cba520232`  
		Last Modified: Wed, 13 Mar 2024 10:09:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c3c23eb3e3b2f254fae58704b688d61c7c1481a14012cd7421f53310564e31`  
		Last Modified: Wed, 13 Mar 2024 10:09:14 GMT  
		Size: 129.0 MB (128991184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381b9a0252cd0d8fb2833fbeb597dfe519122f8926f9152f7e3e55d3d0897c75`  
		Last Modified: Wed, 13 Mar 2024 10:09:10 GMT  
		Size: 1.1 MB (1073409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed83bfae1380a29022abcbaef13497f6e6c4742a85ad37f74d293b392a954bd`  
		Last Modified: Wed, 13 Mar 2024 10:09:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287a1a37d84627e41e295c82fbe4bb6628dcbf5a0ffe79400eed6ddf445fc44`  
		Last Modified: Wed, 13 Mar 2024 10:09:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2b1af35cbea09f8827e75e2e7276134ac3eb369d15817d884768798236b24`  
		Last Modified: Wed, 13 Mar 2024 10:09:11 GMT  
		Size: 3.2 MB (3240612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8137aa558d35aa56e2c86d0b67e10ac63b6a7d09288628bb8b562f9b42b25e32`  
		Last Modified: Wed, 13 Mar 2024 10:09:14 GMT  
		Size: 66.6 MB (66581518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc1533ceaff6971b463950c3fc00e16c2b44149ecaf341ea7bf3665eec8cf27`  
		Last Modified: Wed, 13 Mar 2024 10:09:12 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:9efa9e3ff33f614fe3ee80ba4e9195ed0287ae8889d3b77bd6a500aa80fc499b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8901284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbd993454ae0137b037bf875308bd061b3207dd347970208f4b2f7559e5fea2`

```dockerfile
```

-	Layers:
	-	`sha256:bd4196d855c0db65e74c0aff6db26c4115a8d0f696b2a088f0fbff2c25d38bc5`  
		Last Modified: Wed, 13 Mar 2024 10:09:10 GMT  
		Size: 8.9 MB (8858277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34c90c83a418e409bef12c0fef9aa5384f816639a32636c557ad5426696ed0a`  
		Last Modified: Wed, 13 Mar 2024 10:09:09 GMT  
		Size: 43.0 KB (43007 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:64d535986396cc1b8e8f3a6c0a694fa6633dbc8be16705734ad1f4d6c6b7aaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257826943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b792e3b00afb55a2e14eafe2af842d86124c4527f614d8949af39c0ab54ef8c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d7835885823c3a0a75128f52da3368397ac7dd7ffa0cfe5dd9f6ab6b47cc9`  
		Last Modified: Thu, 14 Mar 2024 06:17:13 GMT  
		Size: 12.0 MB (12024147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5007f54d8fd48606459feeda089ab44ba57e6b659b1a1f899e493428baacd59`  
		Last Modified: Thu, 14 Mar 2024 06:17:12 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174ce6e6bfe69bfbdd1190c41ba4d1f986965a2f012d2a443e82c41334ad0ef2`  
		Last Modified: Thu, 14 Mar 2024 07:01:06 GMT  
		Size: 31.5 MB (31534052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c2edcf63b4a065a390b93c944346358be362f34114b0c11fd3e7519766701`  
		Last Modified: Thu, 14 Mar 2024 07:01:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b58bba230920fd22490c1af9476d4cb6aeaa5721ef51a036194a7af84621cc`  
		Last Modified: Sun, 17 Mar 2024 09:25:02 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee60812e7432b61c9783530de7c351851382f105cc3447160e61aec6914ba785`  
		Last Modified: Sun, 17 Mar 2024 09:25:04 GMT  
		Size: 117.7 MB (117743500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a0fc42279e6675367cab7f186cf6e496c4a9dcb7cf92e1fc663e5d1f3166f`  
		Last Modified: Sun, 17 Mar 2024 09:25:02 GMT  
		Size: 1.1 MB (1117530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fbc1a11ce0f8dbbc7d13aa1da5833d0184d58a0a2b14266b8a71f26b8d8f52`  
		Last Modified: Sun, 17 Mar 2024 09:25:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14d8577a11b86a093dde2705be31b02c0db368faebb80e3bbb01bfd28d891fc`  
		Last Modified: Sun, 17 Mar 2024 09:25:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024727db9d9c60c2e61c4db62855ad456ddf94e719a82c7bab0863ac96de7812`  
		Last Modified: Sun, 17 Mar 2024 09:25:04 GMT  
		Size: 3.2 MB (3240609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49617fab8432228145526acf7e8b83eec632db7c32ff7e02b6846ca1aa694a21`  
		Last Modified: Sun, 17 Mar 2024 09:25:05 GMT  
		Size: 64.7 MB (64674696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7258ee5bb9a435609d2c6790f25b036f89cf734f3a0b8584b10c75b20aa29ed4`  
		Last Modified: Sun, 17 Mar 2024 09:25:04 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:711bd507880625724582396a94cc84a22839dcf17e3a687d01b7a5a6d16486f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8887508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08820f4bbfc901df3136721f82b3299918bee3c145bed32b0102a0f2e9e464fb`

```dockerfile
```

-	Layers:
	-	`sha256:cd3adc2accc00cab9a30cbde397f1ea04f3220b13a1f3399995a1abca21a63f8`  
		Last Modified: Sun, 17 Mar 2024 09:25:02 GMT  
		Size: 8.8 MB (8844639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c1b28c8277254a247bfb7d692c64aa54217cf1ee41d95fd6e26f3d4db77cfcb`  
		Last Modified: Sun, 17 Mar 2024 09:25:02 GMT  
		Size: 42.9 KB (42869 bytes)  
		MIME: application/vnd.in-toto+json
