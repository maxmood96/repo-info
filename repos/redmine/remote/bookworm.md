## `redmine:bookworm`

```console
$ docker pull redmine@sha256:41ad17dbb2bd0c13a9a6651566c253c32fb86234fb1e2bfdfca002a0b52b1a84
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
$ docker pull redmine@sha256:7b887178ec0bedc748c3c35ddfe78a7a53096def08333a0e865e361ecac29503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255351797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83d8bd9215b01c93d216ad691b0f0629a7fea1ff573d6cb159e82ec925b12e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1259e80b1ca04c82c90d80dc4b56f37de725015b6c20946bf3a064dceb7d062b`  
		Last Modified: Tue, 10 Jun 2025 23:51:09 GMT  
		Size: 3.5 MB (3500689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fe40bab7cac19bec9e4638d461509aba010b275268befddf46712c53dbb29`  
		Last Modified: Tue, 10 Jun 2025 23:51:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be325fd3530eea0ca4e34a7763e3fd7c2e324d7241af3df6c6a20a5b58b8c004`  
		Last Modified: Tue, 10 Jun 2025 23:51:13 GMT  
		Size: 37.7 MB (37745803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91615b99d57a824673dcc592cf636f7bdd0e249f79070c27d9e8968bcbab831`  
		Last Modified: Tue, 10 Jun 2025 23:51:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9ede6970583141f6793c4f444b17576c3d937e79f7e4539af7c50db5e2369`  
		Last Modified: Wed, 11 Jun 2025 02:22:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f26435894fba2d85a5e1a7d2a692a170c97f3cf9b19266ca2a8329308972c0d`  
		Last Modified: Wed, 11 Jun 2025 04:50:18 GMT  
		Size: 123.1 MB (123118159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5d6f4b8755d60960c2088ce644fb769db020fe00d570d9b9730b1b63a11fdf`  
		Last Modified: Wed, 11 Jun 2025 02:22:32 GMT  
		Size: 1.1 MB (1143644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55e826954e469dd1fdf9bf5b5edfa75f4d22c635de1a3f4f9c224c812bfd38f`  
		Last Modified: Wed, 11 Jun 2025 02:22:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b0e9ed33052ebdb655363792bb041cb69445808ff1a8e99e88562363e9ca78`  
		Last Modified: Wed, 11 Jun 2025 02:22:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395e45fc56d83a0671ea32e9c462d3fc08df9f6fcdc584775fcaa0a04c2a148b`  
		Last Modified: Wed, 11 Jun 2025 02:22:44 GMT  
		Size: 4.1 MB (4061965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424eac306530d870579fc3b8437e8ee5bd2b6c726aad52c4db6ab86b15195201`  
		Last Modified: Wed, 11 Jun 2025 04:50:17 GMT  
		Size: 57.5 MB (57547396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d3c777204a5a12860003d0e7e5dd77c9e4350bc2f8f1f6623b49437b1ef2c`  
		Last Modified: Wed, 11 Jun 2025 02:24:28 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:704c12b78f03fbe70f4b10140acce2caef6b41023c8af8d5fb966acd3bb21221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d3595035f508f2d95a090d3d3f2413163d9dc1f27faab20845a1958929190c`

```dockerfile
```

-	Layers:
	-	`sha256:a7fdb984d5fa947868b4ba3d500d7655e5f0b2916354a3a0013a9ffa62343785`  
		Last Modified: Wed, 11 Jun 2025 04:49:50 GMT  
		Size: 41.3 KB (41252 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:1841cdd30938ed8d13d6e5d77a713ac406e81c805a0601593333c1427f056f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239750983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048511326e10ea52d77cf4065b5ef0cc24ef2abb8b7963f58c8a1bd4804c7b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64aa76a1aec4ca5ec6b604ac62f2c56609b258965abd5c532f8af0ce5d922f`  
		Last Modified: Tue, 10 Jun 2025 23:45:16 GMT  
		Size: 3.1 MB (3074545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da89e316d2db415892a55dea78835d5fc94fe6541a7f5c6b4b363c41e6a759`  
		Last Modified: Wed, 11 Jun 2025 06:07:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855dc9665897a33f6fa707cb2f451b1086328dd512a2e3a5b0fd2a6c539437ca`  
		Last Modified: Wed, 11 Jun 2025 09:58:32 GMT  
		Size: 34.3 MB (34293534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8226e65e4277b6c15fa376d9c4a77012d16051d2ff8d27808cb87aad2dd6842c`  
		Last Modified: Wed, 11 Jun 2025 06:07:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9246d03f10859ed1e83df144a5208088ccc6c1773f755ff009ff68d0df981b`  
		Last Modified: Wed, 11 Jun 2025 09:24:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6453231d27101828d4b9abf76f051bde23d9ce64b79bff63d6f1ab31878d937a`  
		Last Modified: Wed, 11 Jun 2025 09:24:58 GMT  
		Size: 116.7 MB (116745699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6832415706b4ec1b658de731377310ef857a0374764fae18a11845e7b1b8347`  
		Last Modified: Wed, 11 Jun 2025 09:24:36 GMT  
		Size: 1.1 MB (1120864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8de7ebe68614ea611ec06ebb79108ca1f56a682bbc564fc9885ce6240d78a9`  
		Last Modified: Wed, 11 Jun 2025 09:24:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beac6caf3dcc9468af05f0c23e1ede07ef5abd164dc824dac37c75a263b65abf`  
		Last Modified: Wed, 11 Jun 2025 09:24:36 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9f1756ed9a9111fbf9db238b0f5d582f2d3a8abbcfc76f25aca60f18a0772`  
		Last Modified: Wed, 11 Jun 2025 09:24:37 GMT  
		Size: 4.1 MB (4061968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4beb3b0d9625be32b3ede0c74204d2c9b489051e55e54ab1de538a38648a4c`  
		Last Modified: Wed, 11 Jun 2025 09:24:08 GMT  
		Size: 54.7 MB (54687967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4692aea5ffb0908a460fc72d303a64100d2fe952b3ddfe88096ba26d8d64a8`  
		Last Modified: Wed, 11 Jun 2025 11:21:41 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:92ad66f1b98f05d4bcf99aefdde4105f983a16a3f4418f99c8fdfe231a4727fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65715468245f6ce10fad63e8c0f8daead11c18322475cd9ef4a6189859b3cf00`

```dockerfile
```

-	Layers:
	-	`sha256:bee176d4308fcac9114e78e2f8ae0c7e1064bafb89653ac9d9fa7cfc01544685`  
		Last Modified: Wed, 11 Jun 2025 13:50:02 GMT  
		Size: 41.4 KB (41425 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:1b85c451da31c485ce3a9bbbe9e4f4a6c66af887022e1146e08bc51451b331b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232858793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f9d573a164c5778516743f5faf03354b36d1de729d57ad6f393494e97804fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99f1fd0040c720090a4a658b14eddcebacfa8e9ceea1496ac57e2d4a4473ba6`  
		Last Modified: Tue, 03 Jun 2025 20:01:36 GMT  
		Size: 2.9 MB (2910204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1a61d482bb9702b456bdd78a6e07b19b21b0f8c4047dcd67366728a32f295f`  
		Last Modified: Wed, 04 Jun 2025 05:46:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738d3dcf7567b07ce9c81c335f2560b982a98b56cd8ead0323965a0a7752384c`  
		Last Modified: Wed, 04 Jun 2025 05:46:12 GMT  
		Size: 34.1 MB (34148541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a75f2d060283ec4482b6a5c57eaee08571412ba19b9fcd78dca83558ae80776`  
		Last Modified: Wed, 04 Jun 2025 05:46:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f091e466f0b3cf690f2d780d19922e10eb9bb87556ac46c3e34ffc4a51417cc1`  
		Last Modified: Wed, 04 Jun 2025 13:11:58 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c394966844969a96fc46dce92d2d5b16771bbeac041f3d8936a6c27011ac3475`  
		Last Modified: Wed, 04 Jun 2025 13:26:02 GMT  
		Size: 112.2 MB (112161261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123d5e510813dfd4b22dc05f37f3695a6e304401582732bb5b9ac5f15f578613`  
		Last Modified: Fri, 06 Jun 2025 06:37:03 GMT  
		Size: 1.1 MB (1110091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86eb370164e3022c25e3483629b2dd9a75efca4649b3fd53cc278eea82ac9e0`  
		Last Modified: Fri, 06 Jun 2025 06:37:07 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f8c1dc43929661d3ee9b847e07e59b9d6dc5e1de902642bfe83198a49de2ad`  
		Last Modified: Fri, 06 Jun 2025 06:37:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e106f2103c65d1f7f9cd6a8b7b8426ad4a0b9077acf0459ec0fe25ad4649ff6`  
		Last Modified: Fri, 06 Jun 2025 06:53:21 GMT  
		Size: 4.1 MB (4061968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7b515e3e73dc86223c2ecc37f90ad37f914147562792371ca4319f5bd0ddb6`  
		Last Modified: Fri, 06 Jun 2025 07:04:10 GMT  
		Size: 54.5 MB (54529801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccd74f75c7bfb24e5c6aba259a6dd3330db9bac9a08dc98ae4087c264bb7a06`  
		Last Modified: Fri, 06 Jun 2025 06:53:30 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:e4371b6e7fc479b8ecfd2b33996f28a3489c693896aeb83c886c08f511378c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439a3a285a2b9e0cce04419085672c41fcf20dd89b99696553e909b67476890`

```dockerfile
```

-	Layers:
	-	`sha256:ebb9f55c250116af3635526491a769a850c976ee805c01b485e2d7d39feec58e`  
		Last Modified: Sun, 08 Jun 2025 21:28:36 GMT  
		Size: 41.4 KB (41424 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:cda5b1b22a61a1e4c21009e324537132b0691f6d02d1f1ab06f1c4d39a03fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251588670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47f2a0f5b99852922c0f089dfda58412835961722fbbdcfb6e83743efdd543e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Tue, 03 Jun 2025 13:31:01 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bd6bc7ca0b1d67b661b24fbf46a7691f56dab2d717dfc202a60f1c920c7b9`  
		Last Modified: Tue, 03 Jun 2025 13:31:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18736c36e29aa038ba6dcb36f39616b5e29e420492b1fccd8a23a146ae4fe069`  
		Last Modified: Tue, 03 Jun 2025 14:14:22 GMT  
		Size: 37.7 MB (37734401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786fdd4bc3cb5050381946a7d16d69e8664506c271a6baf2c2dd82eb681c0ff9`  
		Last Modified: Tue, 03 Jun 2025 14:14:08 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10011f4b71c1cf170a2dfb578c62bb53f9d9c3608629b0f989c639946a2e3c9b`  
		Last Modified: Tue, 03 Jun 2025 14:14:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5e27a58f479db754aa13312d6d87502ad78a2a40db096adfa357c36b5d72f5`  
		Last Modified: Tue, 03 Jun 2025 17:51:01 GMT  
		Size: 120.4 MB (120408799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f37d6b00f5f5aca8e7055b24c3ef0ffc45c8c97de88b001c18c2d529baab5`  
		Last Modified: Tue, 03 Jun 2025 14:14:13 GMT  
		Size: 1.1 MB (1076212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c471225db960c52a098cfbf6716a3eb39ce1030ce08c4dc4dae96a7a47190c09`  
		Last Modified: Tue, 03 Jun 2025 14:14:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16b82620cdc6eb0969a491d17ad2f83957ed0f687a1699c23fd0d05773c93f6`  
		Last Modified: Tue, 03 Jun 2025 14:14:22 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23821867c98aa3d564b39fe8f10b906fc04ba7152bd6883f82f10533471ce92a`  
		Last Modified: Tue, 03 Jun 2025 14:14:34 GMT  
		Size: 4.1 MB (4061965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1bd2c6fe4af14df3577d5c13d7b8378b58a74c7dafd8eff4e7af17ad6f1255`  
		Last Modified: Tue, 03 Jun 2025 14:14:43 GMT  
		Size: 56.9 MB (56913612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92a84e1ff06e39f558b36fd4f8e4fc306e36352ee194fc3c35fc789874c866a`  
		Last Modified: Tue, 03 Jun 2025 14:14:38 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:5028f287e9c38a13c2f33ed0be11aae296e363a5f7a70908b28b0547e379fd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cbcf5b8e7201ec717b9a40c97e442ef630fa90cee4e6467c8509172789b0df`

```dockerfile
```

-	Layers:
	-	`sha256:91b1c039e66511f666d7db543dbdce21960c59f5b2b73f6b37e445725748e13b`  
		Last Modified: Sun, 08 Jun 2025 21:29:42 GMT  
		Size: 41.5 KB (41477 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; 386

```console
$ docker pull redmine@sha256:a427a651e19950a143b52c35b4bfeaba811e4a5025f4b6b64a32c13ef7258991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253792262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed309dbd4d16501bd01aa8a449a886e61e8e0775e22f80ee0f5d72bfd0d39140`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c95b597e7c027e6859a83330e6ba3df54e0942e15f66bebe03c0ea5caa20fe`  
		Last Modified: Tue, 10 Jun 2025 23:46:38 GMT  
		Size: 3.5 MB (3506091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3c11d1c2ae95cd81471afd9b269f4c583bec1a344f7ea6e6a33ce960c0fd1`  
		Last Modified: Tue, 10 Jun 2025 23:46:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e424987bc1816332a99c2861f8dfe844d6f24a21a66c07832a9bb1e6ca669c0f`  
		Last Modified: Tue, 10 Jun 2025 23:46:40 GMT  
		Size: 34.1 MB (34083855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ae87668a2b64720e4362e7ebf6f87262ee831b05fd5cd270866628ddc31a9`  
		Last Modified: Tue, 10 Jun 2025 23:46:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00d56fec4cc17cdeadf0edc1e99785cd12d9cf40c16cbc2faa8d753a64aeb`  
		Last Modified: Wed, 11 Jun 2025 00:10:57 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cb500866b6f1c019d0375ee0b6021efdedac64ba95addd2a8bfa4a66869b5a`  
		Last Modified: Wed, 11 Jun 2025 00:11:08 GMT  
		Size: 125.0 MB (124979569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b568b4ad725febafa7ed6c6656aa007231f715dbbc40a1e548abc0b6700568c9`  
		Last Modified: Wed, 11 Jun 2025 00:10:58 GMT  
		Size: 1.1 MB (1119129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533730b9922b3168f2a1b6921058e8bf1585037d4b31bf6d585cf9a598f083f9`  
		Last Modified: Wed, 11 Jun 2025 00:10:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c55db4157607b3af7171939a77bde8a563e2dc87c1ae465e70e313912ceeb1`  
		Last Modified: Wed, 11 Jun 2025 00:10:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617d323953ee8ead5ef3ee7e98a8663567eb6e375ce4bdcbe5734493f2683d67`  
		Last Modified: Wed, 11 Jun 2025 00:10:59 GMT  
		Size: 4.1 MB (4061965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55df29e0c80c31770ccb9d57d97cd1a76ea018ca38ab27299951390b9945b3cf`  
		Last Modified: Wed, 11 Jun 2025 00:11:02 GMT  
		Size: 56.8 MB (56825210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c08360abb11ca224397fa7cec5647e5c1cc5bba2acb98ff6e12005df1675e4`  
		Last Modified: Wed, 11 Jun 2025 00:10:58 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:10326a92972c28019068452f0ea7d138c05b73ed50b8df124d3389074289b5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d34f0675f9c48b08cfb29561f251456c8af2f4e2098e0486fae498e3791e88`

```dockerfile
```

-	Layers:
	-	`sha256:23f2e8cb439f17f30d9bd666a706657acfbdba208003bc6fc33e8f569d96ec78`  
		Last Modified: Wed, 11 Jun 2025 01:50:10 GMT  
		Size: 41.2 KB (41190 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:f6148d317521878d9caeea244bb7230a1edfcbda7e833ea35e0dcb06e99c1063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259573463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f31f36f57157cd0b1a771d9ed52f0df3f3bafb83a9056c6394edcd19e8b625`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65747dc904d40ad67cb8c68d41158cb757807a395c02b6056d6f2867999d7e7`  
		Last Modified: Tue, 03 Jun 2025 18:45:36 GMT  
		Size: 2.9 MB (2897333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3ff108f2d2f48823f867e17ca6fec3efac7e1e08e0624b3c4800a501319150`  
		Last Modified: Sun, 08 Jun 2025 21:32:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf21fa2f3f2b97c492fca8e3629fc3fae1350bb4f2a3bfb8ac0a0ca216e55686`  
		Last Modified: Sun, 08 Jun 2025 21:32:35 GMT  
		Size: 35.5 MB (35458904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe70389a9064181f4ca218af49a595bb26061926cf7aa09ca4f09de67956a15`  
		Last Modified: Sun, 08 Jun 2025 21:32:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9070292f9c5f8b5e3aa6c983e16c36c869bf206f9638118e86ab7e71c68fbb00`  
		Last Modified: Sun, 08 Jun 2025 21:32:38 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a229b545cf38982864031445f38ab26a4cad698d44fb20849e823ed5938cd0db`  
		Last Modified: Sun, 08 Jun 2025 21:33:04 GMT  
		Size: 118.6 MB (118606935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3948adb9967340dbc4cce3013e1d5c52b0f85e81ed7abfe504ae6545d5a859ab`  
		Last Modified: Sun, 08 Jun 2025 21:33:06 GMT  
		Size: 1.0 MB (1030984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af82908a9ff0c992ccb4756bb242314513992327ef9c32124e0a57845eaaec`  
		Last Modified: Sun, 08 Jun 2025 21:33:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a3aeb2c68cbc98229e2aeaed76a989f150ab2e50d3ab80318b58caba00c051`  
		Last Modified: Sun, 08 Jun 2025 21:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e079b9059912d4481d43a798f999b1d74e06e6476504571adeb3f0be2f8c4225`  
		Last Modified: Sun, 08 Jun 2025 21:33:11 GMT  
		Size: 4.1 MB (4061965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5889fa26dd6de3fb5bef92384a8c813b3d61f71ff097af7113de24c442a86735`  
		Last Modified: Sun, 08 Jun 2025 21:33:26 GMT  
		Size: 69.0 MB (69001479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a24a599adc9a06823d62f2cede160fe0a338b66a12bc9484ce5d98462383b1`  
		Last Modified: Sun, 08 Jun 2025 21:33:28 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:44c268d17b5bb23ea50e737252643f9dac36ef9078ecbee3442d3705beb4d129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf5505e49a4dd9c3625678cc68edfc84fa1eaeded9e8e9c4c3f70dbc2fc77c5`

```dockerfile
```

-	Layers:
	-	`sha256:bb51f35c88b406b41df06d5fde41c9403e38adc7cf4d56dd522c36badcfc3e78`  
		Last Modified: Mon, 09 Jun 2025 21:24:10 GMT  
		Size: 41.4 KB (41369 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:bf67ab86f816e35ae12515f846ff6871459dfdf8380bbfe4d03eda9e1e235731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276680500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb032358d56dfc38601e64e35118df035e8222951c8dbe13e735a74d70e8bce0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c23e8b70b76b8ea0de8337d8ad3f29324110bfc586436fb95d2fb99913a45`  
		Last Modified: Tue, 03 Jun 2025 19:05:34 GMT  
		Size: 3.7 MB (3705099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702a40124f1ce5287ac71de3d1c00bbe42516d8496738b9e42d9effc2cf96d39`  
		Last Modified: Mon, 09 Jun 2025 21:24:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf9746e601a35a9a8c64e818d3a82d8b939e3470feb595fe6aa0edee88c9c81`  
		Last Modified: Mon, 09 Jun 2025 21:24:20 GMT  
		Size: 35.8 MB (35831190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29077f9b22271dd51688d4d8a6bd3e782de3092ec50d774f030f83b095821ba4`  
		Last Modified: Mon, 09 Jun 2025 21:24:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b35a1d0ea37092749a6c7b6ff2f3254af8e2258b4295504289f3ab42b2f6e`  
		Last Modified: Mon, 09 Jun 2025 21:24:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc4fbb276b77924302e1fd780db0617cabb39fe00fda5c08b2a65bf7fea351f`  
		Last Modified: Mon, 09 Jun 2025 21:24:40 GMT  
		Size: 130.1 MB (130090555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b3b6e0e40dba45761dc3bd119d4c9ff8a22cee6f0966541c510fc6696db5a`  
		Last Modified: Mon, 09 Jun 2025 21:24:42 GMT  
		Size: 1.1 MB (1066280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f27f57a58c31fb1f265e63d994d7c94bab57cf63679c3497f1c1c2ceec2851`  
		Last Modified: Mon, 09 Jun 2025 21:24:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c75f629da95a7bbd67ad574baa527d270c64747b4415760ec80c0ab738ef936`  
		Last Modified: Mon, 09 Jun 2025 21:24:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e95424dd792d24d4bc08b4fbb50ba3570b84a99054ec7432f08198ae0317a04`  
		Last Modified: Mon, 09 Jun 2025 21:24:46 GMT  
		Size: 4.1 MB (4061968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ecac9676162c8a9042e8bd3450f960819a42b15ad02fdaeba36a0b2e9729ac`  
		Last Modified: Mon, 09 Jun 2025 21:24:56 GMT  
		Size: 69.9 MB (69854489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7897758912ff83c99257b01d7767524b87cf8c829cffa30f7176890b0e3b3248`  
		Last Modified: Mon, 09 Jun 2025 21:24:57 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:159c3bef69f48248792e1b0d4ab139c8c117ec61c6e22291463f37f53db5a596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38685b2ef158b48f4083fda33dc7480113defa3b3bdf97961a281abf6f5a9586`

```dockerfile
```

-	Layers:
	-	`sha256:c1e62a3c42a2896883dd64f6dbddffd5a4a1da21e31662d038aeab71c834e6d1`  
		Last Modified: Mon, 09 Jun 2025 21:25:01 GMT  
		Size: 41.3 KB (41330 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:27d1263ee5d564de2f0138555b390aab175fe41fe4ef2035cb58f5146a38e961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256983054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62cc3a4355640cf68b8b6242e29f536af71da55a7fcff02e647696477fe1b4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 09 Apr 2025 17:03:15 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_VERSION=3.3.8
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Wed, 09 Apr 2025 17:03:15 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 09 Apr 2025 17:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:03:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 09 Apr 2025 17:03:15 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:40:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:40:24 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_VERSION=6.0.5
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Sun, 20 Apr 2025 08:40:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Sun, 20 Apr 2025 08:40:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:40:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:40:24 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:40:24 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd2f706f8f1a993a631532c76c5c812e4efc1a98ac1534a31d6c1a7d4cb32d`  
		Last Modified: Tue, 10 Jun 2025 23:27:39 GMT  
		Size: 3.2 MB (3164919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4bac46fce85a580af396ae663479267e4331a5a2144a2dfe65f916ecdfab0a`  
		Last Modified: Wed, 11 Jun 2025 06:20:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46179af12c02eac5df95aaa739630a82b3b00cfbb50eede839ce17d63d04a30`  
		Last Modified: Wed, 11 Jun 2025 09:58:31 GMT  
		Size: 35.1 MB (35082435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f6d5d87358f0f489e4d500b3c4d7948e6a218a46b27e7075679f13fb5d9ee`  
		Last Modified: Wed, 11 Jun 2025 06:20:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48de08cf0e455cbab8e18bc821e2c80a3dfa5b9bf9280b5c5113e10b33b6a79d`  
		Last Modified: Wed, 11 Jun 2025 12:13:19 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7c3758f95b918d2d0891be869558421d32926b34dd2f60ab4e4cbf048cd2d2`  
		Last Modified: Wed, 11 Jun 2025 12:13:35 GMT  
		Size: 118.8 MB (118783446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f0f3e866ce907c825c38930869f76243b4bb2a284a1f4f347495c472a67586`  
		Last Modified: Wed, 11 Jun 2025 12:13:20 GMT  
		Size: 1.1 MB (1108692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd5fd0c8dc2dd0c24204e2c87fc390e86c857b3daab82d2be776b6208a9b9cc`  
		Last Modified: Wed, 11 Jun 2025 12:13:19 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9045f4f83bdacbbc91fbdddf585f1a244148b0e6dc8270aea19981e90c2e13`  
		Last Modified: Wed, 11 Jun 2025 12:13:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae67c936f72c4719c6689b9b8aee6e3681f4f5b1cdb979bf546a8a70b6847ae`  
		Last Modified: Wed, 11 Jun 2025 12:13:21 GMT  
		Size: 4.1 MB (4061967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618067ad9b26e0bbab106adc1980d6f93e1941df7cc4df4d9add8dd3fed40a4f`  
		Last Modified: Wed, 11 Jun 2025 12:13:29 GMT  
		Size: 67.9 MB (67889736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba375ab60f16b487fd8ff344bc89e3a8a165e48a03f5409ddfbd9f5fcc8d3439`  
		Last Modified: Wed, 11 Jun 2025 12:13:20 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:4467ed0db4c25832142ca792943e724a322fde3ef0b1402952dd4d540e4c13f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28575ffb4ecda4d0682d5107f689b501c0796b7032d31258604616834cb9ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:75725e75bc2f28e74375ba1c567ecd88b9fd2dff2c468b624b9f180f45c09ffc`  
		Last Modified: Wed, 11 Jun 2025 13:50:14 GMT  
		Size: 41.3 KB (41252 bytes)  
		MIME: application/vnd.in-toto+json
