## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:4abbe0d0094ee61ad528192f3a9e5ae48f853f27debe023c894f201a3234669d
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
$ docker pull redmine@sha256:af7c5ffc72352eb9e1d50c444b6b4c2b1178d2e0fd0a33626a515c712df5a9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258479507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d6aa421df23b7cfecd2536863c79ab508c0c62a90ada07d5f397f90cfe5eb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102d07cd7255acecceeb4553e91e0fc90c9646eb797580d584ceb5264cf5be53`  
		Last Modified: Wed, 24 Apr 2024 05:11:45 GMT  
		Size: 13.7 MB (13657866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48702292f6448229fca62fdb6912cef917d0ccf42913137122fb298e0d988c71`  
		Last Modified: Wed, 24 Apr 2024 05:11:44 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13085d3305b9859374d9c1213622ac34a26d9139846c8cc63b0b35893ebe1403`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 34.8 MB (34825816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe4e008cef7988c566832083bf7304668c3f9352ea3bcdbdc7d30be44db42`  
		Last Modified: Wed, 24 Apr 2024 05:11:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e790b270f8567a39a1c524c20859157cc40d12cbcb94fdc2dc638869c205a11`  
		Last Modified: Wed, 24 Apr 2024 05:59:57 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386724d9ab39c865b152fc63976f27384ffaa5aa0e9da2a824a0f22ee0eccc4f`  
		Last Modified: Wed, 24 Apr 2024 06:00:01 GMT  
		Size: 122.2 MB (122152048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561de714b498141772f6ea1020298ad55e3cf29e4060d7cfd3f05f652bd7e1d3`  
		Last Modified: Wed, 24 Apr 2024 05:59:58 GMT  
		Size: 1.2 MB (1152885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5cd19901ad03b27b6a2986cdc65e8237f5eb46e68082ea52ecc7d262f847b7`  
		Last Modified: Wed, 24 Apr 2024 05:59:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3cc552c21f80e9d70e4561d2805cf2b69179d1bca50da77bcb4c9f19d8df4d`  
		Last Modified: Wed, 24 Apr 2024 05:59:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe08b51de30818f228a5514c29aad6983bee7030405ad5d75c15346add3464a`  
		Last Modified: Wed, 24 Apr 2024 05:59:59 GMT  
		Size: 3.2 MB (3240664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0651793182d714a0ccac5ded8147837670d4c39fbcb7836dc3f1eac523f3b21`  
		Last Modified: Wed, 24 Apr 2024 06:00:01 GMT  
		Size: 54.3 MB (54296022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036b3aa4fe98baec95331d4f38e0dedefb2ec4cfc4fa5087257e707551e40f9`  
		Last Modified: Wed, 24 Apr 2024 05:59:59 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:add3fe4b048c1390b95661fb16d2395961d3caab4106c6bd428f2756cd6d9d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8651962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e028e732b06740682cf575e5aae8659d2b168c724aff9c74c6740d6120969f33`

```dockerfile
```

-	Layers:
	-	`sha256:7032dd24dd3dcf48d890577c8b3661a07bd01d56a67ae4eb24fe65f9dd653d6e`  
		Last Modified: Wed, 24 Apr 2024 05:59:58 GMT  
		Size: 8.6 MB (8609060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084060d88ff53b3045abbe5b0b577e99aa495c2af84eb39b86635d06b2839ccf`  
		Last Modified: Wed, 24 Apr 2024 05:59:57 GMT  
		Size: 42.9 KB (42902 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2c37e5457fe06108c2970a862732bc7afd90cdc16fce8f9788a949d9aa0857e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240817770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dabce08b3b224cb3808a44c5333c7744fa9576b84e58970d9c42abbc2fe388`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce0d8daca6dd823c875685e21d5b1a3370eff7592c11024d5d631342aa43e8b`  
		Last Modified: Wed, 24 Apr 2024 23:55:49 GMT  
		Size: 11.4 MB (11414688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a9baf8c4d252126c82f93d597293913a5091a1ec6952aa01a3b04f4a1ca7aa`  
		Last Modified: Wed, 24 Apr 2024 23:55:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c84680df12b5324756a45773897d54a54a8d013ade4b725a2391978b371f81`  
		Last Modified: Thu, 25 Apr 2024 00:12:55 GMT  
		Size: 30.9 MB (30910150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b9d12609e4061096c32b14b59c678bcad747063d69473eeb86bfe9e0afd8f7`  
		Last Modified: Thu, 25 Apr 2024 00:12:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8228e61e1f70c331c9b6c7d1d1dde59510a18d31be7336d9e602f4719a8b6c`  
		Last Modified: Thu, 25 Apr 2024 01:38:10 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b315fcbcc607c6b11a9e628d0783449f2ec05ca615cd790953282df81ba3cda`  
		Last Modified: Thu, 25 Apr 2024 01:38:14 GMT  
		Size: 115.7 MB (115677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ad4ecfb64b9050962d0ebfb26ec6f022f309a9973cafebef81036f86ee077f`  
		Last Modified: Thu, 25 Apr 2024 01:38:11 GMT  
		Size: 1.1 MB (1129365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d16acf5a0afeb4e40165af60b6c933e12f1123f91a606975a6c9401cd6e6b`  
		Last Modified: Thu, 25 Apr 2024 01:38:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b235eb116cfd35b6742992a96f0e5682b38078a3be8ce44288343c36ea86da6`  
		Last Modified: Thu, 25 Apr 2024 01:38:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4c8bab802ac808f1ceb3e41f95d35e95357ff5c51e257945b11ae53d5960ff`  
		Last Modified: Thu, 25 Apr 2024 01:38:13 GMT  
		Size: 3.2 MB (3240697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bdf2949c73202bd118fd78283f773323288687467cb06b32f0f77ce5b31ca0`  
		Last Modified: Thu, 25 Apr 2024 01:38:14 GMT  
		Size: 51.5 MB (51531674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e1a1714ec38fbcb3b389c5d2897787ae73e6f2f0233baaff5b70677bcf584`  
		Last Modified: Tue, 23 Apr 2024 18:11:40 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:825378abeed660f0f82c5916fdfd68d1dd1e1bf3eb9298ee6f4b0ec6b3138555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8616019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdce1c25e75b5cded12a1ea96df24b78988940e73ed24e9bab75863ddc150d7`

```dockerfile
```

-	Layers:
	-	`sha256:ac9bb2d5c9e86e3d716c2803e17fca871e0e4323072f949f04251cae0919294e`  
		Last Modified: Thu, 25 Apr 2024 01:38:11 GMT  
		Size: 8.6 MB (8572884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735bf531f29c75a3fa079347ffde5835997153d4df68ce0d981b229da4a3eeaa`  
		Last Modified: Thu, 25 Apr 2024 01:38:10 GMT  
		Size: 43.1 KB (43135 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:301fcff76e44412f43991763651a74b22d2d0b91c3c925ff0781072ece6e7988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233140400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f9d66073dd4d92ee3eace17b11d9a88ade25bd629aa32d0be409eac38b824f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ccfa8557f9a06a010e319316c7ef656e743f109a166be263e3eb468b8b73`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 10.8 MB (10753023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef82d351ab736db5b88651cc5d2d237c795e5bb13c49d2db3beeb4bfa7a47b17`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2960344d3528e0e96e7a2dac96ea04c7c741b600586234b11bf187d994c59af0`  
		Last Modified: Wed, 24 Apr 2024 23:47:46 GMT  
		Size: 30.8 MB (30750013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dddf800a0fa24fc3ae61e9fc1187a7a127fec52593a1381a44129cd525dddd9`  
		Last Modified: Wed, 24 Apr 2024 23:47:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397e962f7ebabe23f2b579743db640cc36198262c904f36058e57d98c82703b3`  
		Last Modified: Thu, 25 Apr 2024 12:22:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de33da9638e31ef36c5eeb0f6cefcfd69c7ed91e9890c862667e33ec80e9dc`  
		Last Modified: Thu, 25 Apr 2024 12:22:47 GMT  
		Size: 111.2 MB (111164830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b321907352a9c47a14221bc48e6f7e134d010a9d3e3c0b9e1515e3cb35166`  
		Last Modified: Thu, 25 Apr 2024 12:22:44 GMT  
		Size: 1.1 MB (1118921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b0cc3b80e4dc0311d1659ff8c24694be51aeed15af9cb8512ae0b31310beea`  
		Last Modified: Thu, 25 Apr 2024 12:22:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a442df9d34455633c1858a9c411e68fbe61e0f8b17eeba42fb1cfa81136ff2`  
		Last Modified: Thu, 25 Apr 2024 12:22:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131dab50ac318cdc9c2574e0e451c3f5ed4ba810c76821d6e6dea63ebd896e80`  
		Last Modified: Thu, 25 Apr 2024 12:22:46 GMT  
		Size: 3.2 MB (3240666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a4a55e4401f0b51e75a9732bbeaf2af5db0234660cd12cddbc365d80656807`  
		Last Modified: Thu, 25 Apr 2024 12:22:47 GMT  
		Size: 51.4 MB (51368777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2645f26d76669f2da88cc7070e31cbe0826e05b099b460494979774b28ce3f9`  
		Last Modified: Tue, 23 Apr 2024 18:46:47 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:9002d1965c4b9f7a380b37a25673606b9402641fd56b81dcda1f85452a183eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8617438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0fbf661a11f63255463335b032d01e3ef91aa182fb8f1eb3dd5875d109b65`

```dockerfile
```

-	Layers:
	-	`sha256:7a3f81aac721463d8d1fcd2771f4499fc17a77a8d369020f8fbf95a63eaf3c37`  
		Last Modified: Thu, 25 Apr 2024 12:22:44 GMT  
		Size: 8.6 MB (8574304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee354308fe0ebe12f34cba2db8f8ec5dbcb5b5a82ed12bc50fa11a88d3b4094`  
		Last Modified: Thu, 25 Apr 2024 12:22:44 GMT  
		Size: 43.1 KB (43134 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:22d1a09bb25771231428f4c85abf9c1d492dd28ce80b272c8159580e8c4f7053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253838962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d91d1b3ba42d5022b8f8bee0ce6633b78087e71ac49f942c5c116e725543c48`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cd60c1d2b545dbe2c10439e6215af14355a2749e2c983dfef7d3db00f867b1`  
		Last Modified: Thu, 25 Apr 2024 15:41:46 GMT  
		Size: 12.5 MB (12500309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b90ec0aaef9170a29a216d7e1ea6f1452fe0ff679b52c9c83eb118fa0307a4`  
		Last Modified: Thu, 25 Apr 2024 15:41:45 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfd5ca517297e85d50bb0aab3451edbfe67921d09e3dc16a3d4b4528b306f8d`  
		Last Modified: Thu, 25 Apr 2024 16:09:33 GMT  
		Size: 34.8 MB (34783011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d529a157b13188a5a9f1dea8b9ecbc26638b95edbe7f4764c595ec365b0afe4e`  
		Last Modified: Thu, 25 Apr 2024 16:09:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401df02c6f0ea4f0f27bb89ff3e8a48f69d007cc94f600165de89b3ed35fcfff`  
		Last Modified: Fri, 26 Apr 2024 10:34:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cae78f880a851f9515b316c4eaa986392bb2952bf222c174ec01481f890824`  
		Last Modified: Fri, 26 Apr 2024 10:34:15 GMT  
		Size: 119.4 MB (119351681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d2d8f2b9517035cc3a9e5b410e3a5cb8b4c83c5a592b4563b010330343f04`  
		Last Modified: Fri, 26 Apr 2024 10:34:12 GMT  
		Size: 1.1 MB (1084291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800c159d4f8ef42f4f035c969f6334bd2815bea1195adbefc642da209c04c6a7`  
		Last Modified: Fri, 26 Apr 2024 10:34:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979bb3c2aa4d900a967e0257cd06405603031accd84280574207bf8bab144186`  
		Last Modified: Fri, 26 Apr 2024 10:34:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1e811b04c200a9e128920579e89f34c5f4face8d34e0a494eaac779798133`  
		Last Modified: Fri, 26 Apr 2024 10:34:14 GMT  
		Size: 3.2 MB (3240654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334ebf3b8f13c39e1c939b017cf034ff539724753a46aa71b13d0faaa0f6df`  
		Last Modified: Fri, 26 Apr 2024 10:34:15 GMT  
		Size: 53.7 MB (53695353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02bd761ee96e89df15bffd9248a7fe1527e25f35965412aed8ff4b675c486b`  
		Last Modified: Fri, 26 Apr 2024 10:34:14 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:a14d0212da2d90000f57e265218116fedc9cb50b22622b34817960ba600d87e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8629708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e91292c0d96b9f2176d520dadfc9f31bf86e0fb0c2d4e2d87f63c11aa64181f`

```dockerfile
```

-	Layers:
	-	`sha256:40ef78c0a546cc4fb3a6b0678d863a823699c46c48d055a5b34677fd4556752c`  
		Last Modified: Fri, 26 Apr 2024 10:34:13 GMT  
		Size: 8.6 MB (8586722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6838101dcfa9cd7e0a73468412de71818488815ae55b55eb5ee4781ba5a5d42`  
		Last Modified: Fri, 26 Apr 2024 10:34:12 GMT  
		Size: 43.0 KB (42986 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:eea76669e7f73e5c374747f9c4eaaf3a2b9f01d10f608c5f4eb3c5adbde954be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257413462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5745a29dc1741fa8f91d38ef246158063501ad88e030df8eaf02262041c26fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5a2d1c548883241204814f353ab8a62f790388e18e818029fb03ee5346bfee`  
		Last Modified: Tue, 14 May 2024 01:58:11 GMT  
		Size: 13.2 MB (13207856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaa25c3a7b20b9f676791560069f3612eded1b16c92bf6faf5984486169112e`  
		Last Modified: Tue, 14 May 2024 01:58:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0806c0d183898bbb791ae75cb248fd94869eb2f72588471b39c0e8ed14375427`  
		Last Modified: Tue, 14 May 2024 01:58:12 GMT  
		Size: 30.7 MB (30742203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b5f80a9c374931d53729fc740be42f055b4bd84e3208ef7946b2d499efc083`  
		Last Modified: Tue, 14 May 2024 01:58:11 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5456a3b7abb390ed7f0a5e62ec2bf3bde2aaa6b9d55abddefc2b9dc40ca0ed`  
		Last Modified: Tue, 14 May 2024 02:59:53 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2070335cf4de3463ca6a7dde9f83a4479791a36afe9a153419af8fb839f361`  
		Last Modified: Tue, 14 May 2024 02:59:56 GMT  
		Size: 124.0 MB (124018961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f02d4c487cb68fc422c3dc3307abfd2f32744244f682037ba48c8cc61ed1c2`  
		Last Modified: Tue, 14 May 2024 02:59:53 GMT  
		Size: 1.1 MB (1126408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e082cf5ddc296c66a043bcce69304ab364a864303513d1c3f4641f06cee45d4`  
		Last Modified: Tue, 14 May 2024 02:59:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d541000bf174a1ccb1896aea96090fbab76669f01e55c6183cffaa99170ec3f`  
		Last Modified: Tue, 14 May 2024 02:59:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934364e8a9fe2c25ec2d0dc2dbd55e9615e73cb87bd41b89084f232c2bfc477e`  
		Last Modified: Tue, 14 May 2024 02:59:54 GMT  
		Size: 3.2 MB (3240660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9798cc94211d87bc6c542b2e38057281034d12e6d36dce16e604dfbe9a9776cc`  
		Last Modified: Tue, 14 May 2024 02:59:55 GMT  
		Size: 54.9 MB (54911015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8b5b59ef4ab8fb83ebc22d343821849474a91a35bfe3d70ddbd0580ca26109`  
		Last Modified: Tue, 14 May 2024 02:59:54 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:b2255d9608ffb59ef2218963c3aadce19b958a69c736ba087951b780d2d3e88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8645664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fab7e857857f08c943d231767bcc0d01d03b3884d11c8cf007633d85dbe8618`

```dockerfile
```

-	Layers:
	-	`sha256:00f2c0c170d272d724277f92351662aa5a735dfe9577b586c674dcde69bbfcf2`  
		Last Modified: Tue, 14 May 2024 02:59:53 GMT  
		Size: 8.6 MB (8602825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dd8ee3d52a3d080e233ca707bd34534b20bf088fd39c8cf2393889213903423`  
		Last Modified: Tue, 14 May 2024 02:59:53 GMT  
		Size: 42.8 KB (42839 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:8854dd34333957bc2990fe5a56c4df60870758b05b7b2b14432e7fadfe2ac242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261301084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fdccb2a6b478e871c13f20038d3c8103d94b7d48dcde1232a8fdd7416d6d94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b69ab6d4afa3e9cbdc2fcd7197601a659ee0649e4b9238937e4b16f607a53c`  
		Last Modified: Fri, 26 Apr 2024 02:03:10 GMT  
		Size: 12.7 MB (12680068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f4f2808f4c5d8952a6ac44ba81f1d1608060f90ed6c147d3e45c8942f5d85`  
		Last Modified: Fri, 26 Apr 2024 02:03:08 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340ff189c8c9fe1a54d74c2399a39fcc30d6437427f6df539e2793face2f17f7`  
		Last Modified: Fri, 26 Apr 2024 03:05:54 GMT  
		Size: 31.8 MB (31786443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aaca44a6753b5a84a18a2a473b9ad74f3e5333c7be32ca6aa0632e59ce221e`  
		Last Modified: Fri, 26 Apr 2024 03:05:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2336f51c7b00a0890effc6e35a50ec0b8fbd8694f84df9595373eba15a51613`  
		Last Modified: Fri, 26 Apr 2024 07:01:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd72ef80d186623eee4a27353aee93072fd9ea171f239cdbcb1e5d9d80c4a3f`  
		Last Modified: Fri, 26 Apr 2024 07:01:16 GMT  
		Size: 117.6 MB (117617761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bd039f716078f56e9139eb339910c917b96ce3f8519c3ecc042c2c6644c99`  
		Last Modified: Fri, 26 Apr 2024 07:01:05 GMT  
		Size: 1.0 MB (1039909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d67795f5e65528996dd56adb0bfc7a324296f75693d2c471e512c95fc2c55`  
		Last Modified: Fri, 26 Apr 2024 07:01:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a8cc90417463f29693ae90647a4b1d569d7e76fc1314689411b80bc5c92726`  
		Last Modified: Fri, 26 Apr 2024 07:01:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856cfdae8c728d21eb8f4029f306ff08621cbdaafa7e502cbf5187a78ce9d09c`  
		Last Modified: Fri, 26 Apr 2024 07:01:06 GMT  
		Size: 3.2 MB (3240675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3550e7cc8d716bbf88784994475d48342c3750869517833f7343db5a0775cd`  
		Last Modified: Fri, 26 Apr 2024 07:01:13 GMT  
		Size: 65.8 MB (65788325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a8dac469c20535a1c629b83933f693319ed327176dd2bd16d78d838438fbb7`  
		Last Modified: Fri, 26 Apr 2024 07:01:07 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:ff2e74cb2b7c5a2d07094a9f7e8bfb450f88fff97b7e712550fa4779a55d921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 KB (42860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9220b0da85fc04ccfd6cbb37ea672560acf331d1d630a5a134f8f1dca8072dbb`

```dockerfile
```

-	Layers:
	-	`sha256:8a45bac747639050e13da8cdb83da593372afb850801e8e189a8314307018fe3`  
		Last Modified: Fri, 26 Apr 2024 07:01:04 GMT  
		Size: 42.9 KB (42860 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:135e57dd11cd1e407952c0797e53e1c18e6723b8653e2e6fc3cd71dde72ab6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279693689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a1be71ca6fce49f5263ac6dbf8aa6f8514216fe0eeb76c04d7fab3ffa6a8f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c793d842270657a0c983a75e1700e71bc459e9519a8dfcf4ceb56ea892c81b`  
		Last Modified: Thu, 25 Apr 2024 08:31:11 GMT  
		Size: 14.4 MB (14379781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b995b7f0d0a2213bd8d9883eb14646b6d1daba2a3c680814e12491b3aeab7e3`  
		Last Modified: Thu, 25 Apr 2024 08:31:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d29a85df75ef0a533e2d658f43c9a728e6d8491c18db806212b054003ffb8`  
		Last Modified: Thu, 25 Apr 2024 08:44:50 GMT  
		Size: 32.3 MB (32270055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be392449d8c7dabd3a12aaaf9534cab2db74e5141c284a1a32adf7b18150981`  
		Last Modified: Thu, 25 Apr 2024 08:44:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cef9d67ae81074c424c232f1623530fd589c3df875727125c04baee0f29e3a`  
		Last Modified: Thu, 25 Apr 2024 11:28:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259198e0b98062cb39fa7821bb0d693d24724aec41952db3c686d9116ecd4839`  
		Last Modified: Thu, 25 Apr 2024 11:28:38 GMT  
		Size: 129.0 MB (128997568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44d0d0ee20bd96c11d9bda03817b7cf5b88f14f0cd206eb6444195797ec902`  
		Last Modified: Thu, 25 Apr 2024 11:28:34 GMT  
		Size: 1.1 MB (1073071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bc5df7e9505a84defc2956d3d7b7f30c27b606bd8fc21f4d7f708b650aed1e`  
		Last Modified: Thu, 25 Apr 2024 11:28:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0b606acd7a597afaf5576007f756d4788f206839412a9c92e7801be70201a`  
		Last Modified: Thu, 25 Apr 2024 11:28:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db2ea830789fa9b5b777dd4e8f18fed66abea1929f932d38e517cab07b0570`  
		Last Modified: Thu, 25 Apr 2024 11:28:36 GMT  
		Size: 3.2 MB (3240662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522f4362ff0206281ddd1ae8da4be42c9103f56182a440c0e6a95b3c8b7b2c7f`  
		Last Modified: Thu, 25 Apr 2024 11:28:38 GMT  
		Size: 66.6 MB (66587627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113112bf080be5e0f9293b30de265603aad5593c9d4bb284f17ae5a7909e479a`  
		Last Modified: Tue, 23 Apr 2024 19:16:46 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:bd008a32138d9fd3457f3c5935a04475d5c86c24fb8e313b93b43f99298d47b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8650228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb4cf4fd3881333cfc40fc6dd7143d9509fb6cfe66329f15024f53d0fdee91a`

```dockerfile
```

-	Layers:
	-	`sha256:31b2f2daadf8a596ad94df352e0a17cdd0b4a5c7315af5c3aa94b98d5876ea61`  
		Last Modified: Thu, 25 Apr 2024 11:28:34 GMT  
		Size: 8.6 MB (8607188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562bc59b45ae7bb182091081ef5f39a82cc9d7b058840360337b6655367e635a`  
		Last Modified: Thu, 25 Apr 2024 11:28:34 GMT  
		Size: 43.0 KB (43040 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:53babb30208db6fea40ec2a7273653f44a8d54914d2fd93b13fdf0dbddb2300b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257675390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac03032aa23f3bb9048d177393670d8273d52b8e51cdcb4ebe2b53b48ca35aed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Apr 2024 21:46:42 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_VERSION=3.2.4
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:46:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:46:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["irb"]
# Fri, 05 Apr 2024 21:46:42 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV RAILS_ENV=production
# Fri, 05 Apr 2024 21:46:42 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
ENV HOME=/home/redmine
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_VERSION=5.1.2
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Fri, 05 Apr 2024 21:46:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Apr 2024 21:46:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Apr 2024 21:46:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:46:42 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Apr 2024 21:46:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591a904e1b4f23aebba8e417eb670c1bd4d6703d5a1d9bb5e8cd163ad429bbe3`  
		Last Modified: Thu, 25 Apr 2024 08:47:34 GMT  
		Size: 11.8 MB (11832584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e32ce10cf740d787606c1c7ba7d44ab324de29d20d1e832d57cd1ff5bf29473`  
		Last Modified: Thu, 25 Apr 2024 08:47:33 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff8e4ac450adab632804a13e1b8a49a66e77ae8948d80a449d9a906af825e12`  
		Last Modified: Thu, 25 Apr 2024 09:24:48 GMT  
		Size: 31.5 MB (31542989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20e5e3f4abfc2ea568dc1b5c17a07b9b70fb458a0840266331dbb445326017`  
		Last Modified: Thu, 25 Apr 2024 09:24:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de04eea29ec21e8282a29595a997b33e7ea0e26b05defe343f3906496292c949`  
		Last Modified: Thu, 25 Apr 2024 12:20:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84b58abd27b8a1e4c97efc533f57523b39353e27629b33b9b31bf2e89a817fe`  
		Last Modified: Thu, 25 Apr 2024 12:20:32 GMT  
		Size: 117.7 MB (117746065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6882c22e437d91bba630224520de692b413106009993963fca158cb2936e2bb`  
		Last Modified: Thu, 25 Apr 2024 12:20:32 GMT  
		Size: 1.1 MB (1118141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11378060365bef94ec31be33e3629add19d237ddac9d1955d0da30ea07388d79`  
		Last Modified: Thu, 25 Apr 2024 12:20:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdd997ca0a0997956ce5cd63c8d240f4af817e8a531d30f064cfd3c0cc017dc`  
		Last Modified: Thu, 25 Apr 2024 12:20:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2865ebde3d75e3c23bbb0dd1f19d78e8e5a4db64dbbe8498212843a285b4266`  
		Last Modified: Thu, 25 Apr 2024 12:20:32 GMT  
		Size: 3.2 MB (3240696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06b3c0de813494eb5bb3f41cb47f8662999d636c290844a46029b3a364bc66`  
		Last Modified: Thu, 25 Apr 2024 12:20:33 GMT  
		Size: 64.7 MB (64678835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636fbf38b210a4659edc208f9873aa3b8080ec5ddf815b53c97a7a6ff4facc50`  
		Last Modified: Wed, 24 Apr 2024 01:28:08 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:f2dea92ffb5cca50da6ef01391841edb2bd6c3ad968ee7cc976c4681f93aea70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8636508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024c05b5faa0c3388dd57c90ee2b422b07b01fad20a923c34b358137791dc551`

```dockerfile
```

-	Layers:
	-	`sha256:691548bf7cc53d8a0199d61de48b490b4c678d293ff19b299ffff94cbb113fa1`  
		Last Modified: Thu, 25 Apr 2024 12:20:30 GMT  
		Size: 8.6 MB (8593546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e5852851465394b6d19e9cf1c6d046903dfc646080373c66da5aeb66cc55b1`  
		Last Modified: Thu, 25 Apr 2024 12:20:30 GMT  
		Size: 43.0 KB (42962 bytes)  
		MIME: application/vnd.in-toto+json
