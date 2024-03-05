## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:03b5740eb47c6a51b17395661d4cebf8a8c8e3dad2c58046fa037ddd6971b29c
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
$ docker pull redmine@sha256:af9dc476ebd2ec1d18731052f0961a51469e66cfcc4aa7b9fe540d6d1604a0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258627548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f75a9cb1bca46b509ec4e042b22b53a48adc93a15d990c2ff2bf947d6c438e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65377675c837609b5fa11b4c1f460d2737680c61eff2f4b45c7e60283e1cc4`  
		Last Modified: Tue, 13 Feb 2024 01:57:48 GMT  
		Size: 13.8 MB (13848792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f870de51c24d2eaedf07b5d72716fe6c2cec8f812e84bd438a55398754ac90`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233015afb9fd92818e0b98863648d606d097e984050b4acdd5d318624070fb4`  
		Last Modified: Tue, 13 Feb 2024 01:57:48 GMT  
		Size: 34.8 MB (34816443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb14e612517b832a7bb5a067ab013e1c4f6628a65a8a10cfd7733b9ee95a9b6`  
		Last Modified: Tue, 13 Feb 2024 01:57:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e17848b4149b1300ba51ba1f59704e1f8a0789f637d17ed602f622bc85c388`  
		Last Modified: Tue, 05 Mar 2024 00:50:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94f1f7aad6b653a9b031454cf28edb5f3b58a90170cc53f5bad0debe26dca7`  
		Last Modified: Tue, 05 Mar 2024 00:50:53 GMT  
		Size: 122.1 MB (122149220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976e03de54cdb0808edac7b7563f6ef290782426e89a3a2a9267e53dbd044398`  
		Last Modified: Tue, 05 Mar 2024 00:50:52 GMT  
		Size: 1.2 MB (1152946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c23b2725a34b9eba408331c855a8a54116a70a52c37da0d63eac42d1fe7060`  
		Last Modified: Tue, 05 Mar 2024 00:50:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e1b4aad8c9ca8ca4fe24ed526aee6e13d908cdda04ab4287d60ed3b4d74fe`  
		Last Modified: Tue, 05 Mar 2024 00:50:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5a3bcf8c15a24abd060afab25c247b1d2fd57a0af90b593753bdccd1b88abb`  
		Last Modified: Tue, 05 Mar 2024 00:50:53 GMT  
		Size: 3.2 MB (3240606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5664792e5eec4a39db281d06556723d7db42fa7aad6460ede0e2b31e1c6bb6b9`  
		Last Modified: Tue, 05 Mar 2024 00:50:54 GMT  
		Size: 54.3 MB (54291729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c9359582524896d552f7799aeb063179bb14b77eb9273b528102bb96b36d97`  
		Last Modified: Tue, 05 Mar 2024 00:50:53 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:8dd8dab552d87d59ccc4440340713beddb9f0786f966add3a178b0d8845d5b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8900581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b320daa92f9dd095b81ac56e5850f3f695a3cefe9ca1d27ca5769073c815d9`

```dockerfile
```

-	Layers:
	-	`sha256:06407e7d8875d53953997548ef08d0e2bf97cd8421b34c212e239802c89f4c2e`  
		Last Modified: Tue, 05 Mar 2024 00:50:52 GMT  
		Size: 8.9 MB (8857712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c9142ec0eda204b75c9d13b80ba69a39fee4cd4e35d604eeb42ebd6d577900`  
		Last Modified: Tue, 05 Mar 2024 00:50:52 GMT  
		Size: 42.9 KB (42869 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:10a4fff0dfd5fc42bb731b6c0763b661341a115c3b6bbc92cd13912138f5e44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240960115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b7bc4cee44005d83fcdf7bf9e3b402a34adbcb876efa6e87caa839ab6476f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903327804c1d20548df652abc83c1314c8f83bcc4a284e65ce3bd2968f2e8cdb`  
		Last Modified: Wed, 14 Feb 2024 02:30:12 GMT  
		Size: 11.6 MB (11606628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec40278b157a471803de6ee6ac361bf4c07b174824e6e59a2b21ef86bace8cd`  
		Last Modified: Wed, 14 Feb 2024 02:30:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b238abde91c5b4a8b8ced2109964083d20d735b7975aae2fef214859b9433727`  
		Last Modified: Wed, 14 Feb 2024 02:44:54 GMT  
		Size: 30.9 MB (30905781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473677dda77e7c31bbb079cdb0bd9425d8d4d30b6708beef4da57275913a7062`  
		Last Modified: Wed, 14 Feb 2024 02:44:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86bd16daf34891c374a59cdc2503aff7e548d5369451bf041975c6b20ced7a5`  
		Last Modified: Wed, 14 Feb 2024 21:19:21 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed5ca048957e3ab37ec64d4a0cfe08d9c0895b5251fae0c386ebf5cb8b1f461`  
		Last Modified: Wed, 14 Feb 2024 21:19:24 GMT  
		Size: 115.7 MB (115669379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae37efab0a0156a5257bbc7c4ff7118583a537ff34ca7a2c649311f1bc863c8f`  
		Last Modified: Wed, 14 Feb 2024 21:19:21 GMT  
		Size: 1.1 MB (1129454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79367164025ca8f1c98ad112bcbeaa786d86ae5d9aa72aa067233b6dce5c803d`  
		Last Modified: Wed, 14 Feb 2024 21:19:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f2921c00f6222c0f3a3cf2063ac88db8e9e7a5fe2bb8959fc9c11ca5a99c82`  
		Last Modified: Wed, 14 Feb 2024 21:19:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe2db02ca30c4d919ca55ea08cc0c3f01d7e3877dd02525b3084b6343f8db0`  
		Last Modified: Tue, 05 Mar 2024 01:35:30 GMT  
		Size: 3.2 MB (3240594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709cb327f8628a0ba7721d2f66c120e8215affc6d76b8eca5634d2b18620a844`  
		Last Modified: Tue, 05 Mar 2024 01:35:32 GMT  
		Size: 51.5 MB (51520655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10af97d31e5c3a08ce407543b271f53a4bf1629aa5303746142f64836c359f9`  
		Last Modified: Tue, 05 Mar 2024 01:35:29 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:01a9321d5981d5e53e4a42dfa9ae57aaf57cbb11b1e051fb4f89376631d3d045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8863753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deff0179a60068427f72383876585e8a98958046af1083d0f2254c2648dac445`

```dockerfile
```

-	Layers:
	-	`sha256:98f57a7be4b2c15b2413406c2bf3e2640cc995d72af154e877fd1daa41955249`  
		Last Modified: Tue, 05 Mar 2024 01:35:30 GMT  
		Size: 8.8 MB (8821444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f89a2250e309997113bbb7e601731857c7b10828d1e9b1748bfa45309074a54`  
		Last Modified: Tue, 05 Mar 2024 01:35:29 GMT  
		Size: 42.3 KB (42309 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:5fbed5c904b82ce377e5748716f416c3ad7e8104f0ccf90632c1c806e6d1c481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233278762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2aa34b9b8f4ab14efcda9526c51c5e18b55e4a558d9fef71d166afc4a5221a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Jan 2024 19:02:57 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_VERSION=3.2.3
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 19:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["irb"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RAILS_ENV=production
# Fri, 05 Jan 2024 19:02:57 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
ENV HOME=/home/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_VERSION=5.1.1
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Jan 2024 19:02:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Jan 2024 19:02:57 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cd7f6f50830508b3606bef5ecedde55f165196fa68c2cacba3c414970dadfa`  
		Last Modified: Fri, 16 Feb 2024 05:21:19 GMT  
		Size: 10.9 MB (10943883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07418fa346adfc0361d00e3b665f7343beb109cee260fb657cd7cbed17ab6c82`  
		Last Modified: Fri, 16 Feb 2024 05:21:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f056a7fed8ba213eaefe759c9626f63d72f9ac7984e043fc63fe6ee5d2b71f7`  
		Last Modified: Fri, 16 Feb 2024 11:25:05 GMT  
		Size: 30.7 MB (30740995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d246535e251dd84cf76c1e660cc1894322993fbd56fa2a853271f6c0dfbc4`  
		Last Modified: Fri, 16 Feb 2024 11:25:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fed0538b531901437771becdc7ddad5f8d593b122654fe2202f8459f0bd46`  
		Last Modified: Sat, 17 Feb 2024 08:21:19 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e783c549eee4fc86893d15e14e1bbe3fb3fca5d0e16832e359da3bdd0960ab`  
		Last Modified: Sat, 17 Feb 2024 08:21:22 GMT  
		Size: 111.2 MB (111156002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70e02f6fd930cdd0ea4c22ed0597afa9f5be6d166e9e6c72151f0d2bce633a`  
		Last Modified: Sat, 17 Feb 2024 08:21:19 GMT  
		Size: 1.1 MB (1119060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa865f9d5a0561239a0e64cb2a921b81531f71636b17a7c691f77d524560a2e1`  
		Last Modified: Sat, 17 Feb 2024 08:21:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461b3867e137e87e689f7fc92f1a17dc0fd666763772d482f561a5abf13b5a2`  
		Last Modified: Sat, 17 Feb 2024 08:21:20 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd0869bb118006c43ecc9f0813899f3acb1ee7606ab61431c8c53c1af674df`  
		Last Modified: Sat, 17 Feb 2024 08:21:20 GMT  
		Size: 3.2 MB (3235223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0074fc47b29a4b009f72677119d641d612279c4732f9657ecf986c92a0a8d6`  
		Last Modified: Sat, 17 Feb 2024 08:21:22 GMT  
		Size: 51.4 MB (51363231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5780441e2c6f621b2cb8c2dc102bbb6e113574dd2eca70327d4b0f088eb585b1`  
		Last Modified: Sat, 17 Feb 2024 08:21:21 GMT  
		Size: 2.0 KB (2010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:0100abaf41ee23e7eb254415e096ad25509907e66c7c125721bd085c44349caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8865607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04fb0cdee94ca192f51f7d2a7966cd366f8ec1314840f78f759c13e8db41af9`

```dockerfile
```

-	Layers:
	-	`sha256:4bbc2ecc8a2e5765da9269333deabc976960592814e6372ea56a5a8fe86dba50`  
		Last Modified: Sat, 17 Feb 2024 08:21:19 GMT  
		Size: 8.8 MB (8822505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d003113e7949af9f65b2d95adb826a9df0f39cc18a751e011d251b7e7a39913`  
		Last Modified: Sat, 17 Feb 2024 08:21:19 GMT  
		Size: 43.1 KB (43102 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:f8af91f24e1cc50c7a70b71777882b6ee53288cb09fa5fea7507bbca7825f18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254016138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6bb7f599879f33d177c5fe24983b73de02e7b4f13450d154b8d97b06cf581`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Jan 2024 19:02:57 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_VERSION=3.2.3
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 19:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["irb"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RAILS_ENV=production
# Fri, 05 Jan 2024 19:02:57 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
ENV HOME=/home/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_VERSION=5.1.1
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Jan 2024 19:02:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Jan 2024 19:02:57 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a1158a666a02624fee2386e375eb186da84743bbd36b13bef256dfbc13af6d`  
		Last Modified: Wed, 14 Feb 2024 08:17:14 GMT  
		Size: 12.7 MB (12689872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368d332d7b2f2af9d6f3a841ca2d277e9c717b56119303170d643fa2ea80af1f`  
		Last Modified: Wed, 14 Feb 2024 08:17:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45132b618903018d406720176fe5275dd51ae92dbf0abc749efd171e18b2ef`  
		Last Modified: Wed, 14 Feb 2024 08:50:14 GMT  
		Size: 34.8 MB (34780858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d25921a700042e12485ad14eb16fb3ea99c4c113fe7ef6d06ff705d48573b`  
		Last Modified: Wed, 14 Feb 2024 08:50:13 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a81dc6d62d49e68716ecff687e80e52cdcbba4d8f814ff7bdbfbc6f998216`  
		Last Modified: Wed, 14 Feb 2024 11:39:37 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cfc026dddda3c081568e212807682495a290b3867dcbb1812763d00fb940d1`  
		Last Modified: Wed, 14 Feb 2024 11:39:41 GMT  
		Size: 119.3 MB (119347725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c880fe820011d07771efb26956f8b0581c823aa20b2851273c592445434cda7`  
		Last Modified: Wed, 14 Feb 2024 11:39:38 GMT  
		Size: 1.1 MB (1084246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1a5a5261128da7efd1da58ad6676a2f7715ecf8e0f84717360876a8bfdad2c`  
		Last Modified: Wed, 14 Feb 2024 11:39:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad5393fa962473cb4038c24d11e1f66dcd90d22e8d5c6fd88a0eac19026aeb7`  
		Last Modified: Wed, 14 Feb 2024 11:39:38 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2228618116f6c0727e43560f3d13eb3f20c6f37eca48aa4260f4b71aa6c7c6`  
		Last Modified: Wed, 14 Feb 2024 11:39:39 GMT  
		Size: 3.2 MB (3235226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193434ade29038c695f71fbe49e3510c29ce1981bfdc07e3e1dae78392d850b2`  
		Last Modified: Wed, 14 Feb 2024 11:39:40 GMT  
		Size: 53.7 MB (53718127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd78565a97ba697b3a462b6c1869eb04bb453d3f2d8ce51b2c799711ed7696c0`  
		Last Modified: Wed, 14 Feb 2024 11:39:39 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:5dfe1a7792aae14f811da777c2146286f85c97189fa3fbda5644f0c90513eb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7822344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53de2f0813937ba68247d31c3715a8718897f9100e11ea80fd68883c3d87690`

```dockerfile
```

-	Layers:
	-	`sha256:e139b90858bef87f3d808af0b44a61607e6b51270a4de77e18c0dcca9e2c2b5f`  
		Last Modified: Wed, 14 Feb 2024 11:39:38 GMT  
		Size: 7.8 MB (7779391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d79b9d91e05b9fd6bf5da16584d985d0eee1bc8e49b2dd7bfe6f3637f2ec9c`  
		Last Modified: Wed, 14 Feb 2024 11:39:37 GMT  
		Size: 43.0 KB (42953 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:713169a0973559a41bd735c65f6bd6530aa30af5f6df1740cbe29ec39a1d5cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257596983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf593bd92d1e5addec589626983091cd05c9794a210d15f10b05f6f623dc1d35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Jan 2024 19:02:57 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_VERSION=3.2.3
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 19:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["irb"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RAILS_ENV=production
# Fri, 05 Jan 2024 19:02:57 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
ENV HOME=/home/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_VERSION=5.1.1
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Jan 2024 19:02:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Jan 2024 19:02:57 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee529a5d44eb84e4d1a6b3713fb709fab50c9be2b3400e6f4bce8d542d16df1`  
		Last Modified: Tue, 13 Feb 2024 01:57:50 GMT  
		Size: 13.4 MB (13396841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f0a9e9d6799775e78cd4c94516d5c13f0bb4c29a2361bd130c1160faa1ff79`  
		Last Modified: Tue, 13 Feb 2024 01:57:49 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbf05ba12e8dc8dda24045407b215da1a9e941dd692dde4aa07fcf669920d5`  
		Last Modified: Tue, 13 Feb 2024 01:57:51 GMT  
		Size: 30.7 MB (30737125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912e095970e9613e35fb5fd06cfa1b49c5d0df8ae44c67c88e37cfd8e5680467`  
		Last Modified: Tue, 13 Feb 2024 01:57:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238cfa5957d9c02aba52d5d196b39c23c156553bf37253be61b58273b983ac7f`  
		Last Modified: Tue, 13 Feb 2024 03:07:02 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a54d1ed7381c60d6ac6345f5774f148535db5ad595bc0308009064d35e54f2`  
		Last Modified: Tue, 13 Feb 2024 03:07:05 GMT  
		Size: 124.0 MB (124003456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac4b9fb27986588f1c891b2bf01ae03f4f02a25110b1bddb942277768e7371e`  
		Last Modified: Tue, 13 Feb 2024 03:07:02 GMT  
		Size: 1.1 MB (1126329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e6741446a7c477a653a4a53faa461dbf37fba3c4c9eb491c18b8dd2d77e938`  
		Last Modified: Tue, 13 Feb 2024 03:07:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd395e2ea9f504efa0b0de44cbb1426999242ce8515040d4a4ab35d8db420d`  
		Last Modified: Tue, 13 Feb 2024 03:07:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3402aca9a586f3efb5394a6f4f485b986be646609884b4790ca68e0f651e6`  
		Last Modified: Tue, 13 Feb 2024 03:07:03 GMT  
		Size: 3.2 MB (3235216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b820f8b401a79196fc3cf3aeec9802babc727f0de7f28b8c4d93498ef1cdff7`  
		Last Modified: Tue, 13 Feb 2024 03:07:05 GMT  
		Size: 55.0 MB (54952483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b07464efae5a6f0df80931563f09d3c9642c82fec232e81d744ae61459ba154`  
		Last Modified: Tue, 13 Feb 2024 03:07:04 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:aacba1ae8e717623b8825f136f687016bf892fe5a3b4ee3dfe45d061a7ae7858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7833776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a324ee065d97ec3c4544359364c01002fba4e4cdce12927d30ebaa3660d884`

```dockerfile
```

-	Layers:
	-	`sha256:7c4e95e4cb5676448a5fd5cb557804e4809c9010b5ba94a155c46b7a505226a3`  
		Last Modified: Tue, 13 Feb 2024 03:07:02 GMT  
		Size: 7.8 MB (7790970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b41b8a89c3cdf3f784b6d111916a809f9aff3c2a711d54b19aefb4959a2b889`  
		Last Modified: Tue, 13 Feb 2024 03:07:02 GMT  
		Size: 42.8 KB (42806 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:424e5f90147d31d0094ce1a4d2d4c8e989dac3db0a52be2c0b88b36715e950e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261472553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bf2e0507f934dcf8c3954f5d9ae312921c8a5d5e9f95b03537e49c5526978c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Jan 2024 19:02:57 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_VERSION=3.2.3
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 19:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["irb"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RAILS_ENV=production
# Fri, 05 Jan 2024 19:02:57 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
ENV HOME=/home/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_VERSION=5.1.1
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Jan 2024 19:02:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Jan 2024 19:02:57 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2d5f7d0d7bb1cdf4a89d1ce764fef397d7513c546cafc969ccfb0e6144b81`  
		Last Modified: Thu, 15 Feb 2024 06:01:41 GMT  
		Size: 12.9 MB (12871140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d43c864445d77efb31564db7ab9422723cd688d9275ab66d07aacc3c2ed9d88`  
		Last Modified: Thu, 15 Feb 2024 06:01:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de54e61706a0c82a8ca7615d14eb32dca2e31d4b7da8ff5b2ca6b6b85f50dc4`  
		Last Modified: Thu, 15 Feb 2024 07:04:33 GMT  
		Size: 31.8 MB (31774917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862a4ab354438424ba874646076ba4806a9ef5b0b801742c99c80ea1da6dcab`  
		Last Modified: Thu, 15 Feb 2024 07:04:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aade82b2fc3a957dd18aac70d2821b9a0dfc4caf287e3d47413046eb81739b7`  
		Last Modified: Thu, 15 Feb 2024 11:31:29 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5802f40f4afac09ea0602cf61d3d0649456638828d12a376191a7a0072a3a04f`  
		Last Modified: Thu, 15 Feb 2024 11:31:40 GMT  
		Size: 117.6 MB (117621854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167f6c0116f11c1a833770557291a9070d96aa43aacee78d9a36bf697f6fcd86`  
		Last Modified: Thu, 15 Feb 2024 11:31:30 GMT  
		Size: 1.0 MB (1040050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1196d9e8496f6a463f2e2fe4433d2a7aa897186740b3e9cf914f5084df197315`  
		Last Modified: Thu, 15 Feb 2024 11:31:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0ec7a4e0eceee8e48fb0f33b9e262341947f07181d0e6ef40a5ed8680ad654`  
		Last Modified: Thu, 15 Feb 2024 11:31:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c433ed3e2b2d83565c5436042c7f2792213f99494b360dd96651cc10a5c1d97a`  
		Last Modified: Thu, 15 Feb 2024 11:31:31 GMT  
		Size: 3.2 MB (3235223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc1174ce16e7dc783cb96392df98b7b35b163ebc1d03e4e23dd1b6c22ce8d3`  
		Last Modified: Thu, 15 Feb 2024 11:31:38 GMT  
		Size: 65.8 MB (65806553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf32d568af79e90d1a7c4ec468cc2bffeb118a979550c2c21754708da30a3e0`  
		Last Modified: Thu, 15 Feb 2024 11:31:32 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:6c8aac5930043fd854c1c0437018470c6b713efa4b68f331a39ba84c16c1f077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 KB (42831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d29d21d5f8c8e32192af4e4ce9d42654fe4eabeab743fd9c28c76d8b2526e9`

```dockerfile
```

-	Layers:
	-	`sha256:66e65f94333da4123afd106958b57fbe213d7c6c7b6804e49bb6c5ad24f33171`  
		Last Modified: Thu, 15 Feb 2024 11:31:29 GMT  
		Size: 42.8 KB (42831 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:95a5d89c2ee3ae0ff3b9bed8bda0a5e508d7f041804768f5a6a4ae907ea5429d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279865972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bfa5940e4fb422ec6b42c63589db0b3a1b1f9152265318afb3b323ba788e431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 05 Jan 2024 19:02:57 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_VERSION=3.2.3
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Jan 2024 19:02:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 19:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["irb"]
# Fri, 05 Jan 2024 19:02:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV RAILS_ENV=production
# Fri, 05 Jan 2024 19:02:57 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
ENV HOME=/home/redmine
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_VERSION=5.1.1
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Fri, 05 Jan 2024 19:02:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Jan 2024 19:02:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Jan 2024 19:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Jan 2024 19:02:57 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Jan 2024 19:02:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f3efaf93ada710c7a18c1ae70de6b95212aaf6aeccc080e1b45a649c129b42`  
		Last Modified: Wed, 14 Feb 2024 04:35:58 GMT  
		Size: 14.6 MB (14569762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaba8b65e414e671991ef428e47c89f695b46f52424cdf020c8de9529c5fe7d`  
		Last Modified: Wed, 14 Feb 2024 04:35:57 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3597a63202a4a42eace7ab060ee836b29dd1a817850adcec9655a9385cf3fb`  
		Last Modified: Wed, 14 Feb 2024 04:49:19 GMT  
		Size: 32.3 MB (32266267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39beab90d2b39092e295439f948b8c749afa13914c25db7b78e8102a5a571afe`  
		Last Modified: Wed, 14 Feb 2024 04:49:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c7eebc30457108afbfe67baa817c4ecd941ab1fb2f5f00e62cec72f4f74b6e`  
		Last Modified: Wed, 14 Feb 2024 06:47:13 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a843569bb1edeb512e8475c474b5cdbe1991d9f43c98a80b506f1ef4338b9f5`  
		Last Modified: Wed, 14 Feb 2024 06:47:18 GMT  
		Size: 129.0 MB (128998389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254c4216753789c79ca42c4cc1ea84e0d924e9d40c67df6e8ff82b4a5211ffe1`  
		Last Modified: Wed, 14 Feb 2024 06:47:14 GMT  
		Size: 1.1 MB (1072989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dfe0af40043a9de978c7ef8997bb5cb513c47c28739dabed73a3eb4197dd8e`  
		Last Modified: Wed, 14 Feb 2024 06:47:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8edfe74d8bdbb37fa1201e2c347f5a810eb78ab98774938d2c50fa46034f6a`  
		Last Modified: Wed, 14 Feb 2024 06:47:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a09d1ddf05485f8d7990eab0284d95965dd0f0aa33c2716b2861574bdbd92c`  
		Last Modified: Wed, 14 Feb 2024 06:47:15 GMT  
		Size: 3.2 MB (3235219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5581a29022069d00c552645dc58e99443c1f7184c431b59c64ec66946d5e4947`  
		Last Modified: Wed, 14 Feb 2024 06:47:17 GMT  
		Size: 66.6 MB (66600712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29eba30a02301d4c03bd80f3e92a942e5695f26b85d77dfd0ea85b7f54b49489`  
		Last Modified: Wed, 14 Feb 2024 06:47:16 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:fc438b0337b8886b6f2cba9e2923e910bee9911314aed52a75e09d6b7e3e1112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7844449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f3f58a76c3087fbd406b4812448bb003a54102090cb19adc5ee1acf6aacab2`

```dockerfile
```

-	Layers:
	-	`sha256:73adde136b70de353e88112817579288f3cb545d86c35d905e5d7709208476c6`  
		Last Modified: Wed, 14 Feb 2024 06:47:14 GMT  
		Size: 7.8 MB (7801442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63866f91e0ed8b89a7b40a1c2f8f5014a43f7b6d42cdbeada5999ac6813da6d`  
		Last Modified: Wed, 14 Feb 2024 06:47:13 GMT  
		Size: 43.0 KB (43007 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:afa2b46138788c9dfbb6ee729f26a9ae42af1bb3a0f4c24626046fe5b02244a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257821701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6407eb74dc593c9dc64a42bf4df2c386e00d24c1d4438a1e6f8a2e97e6148b90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
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
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589785e8a5bc3c7378df2d479b94e4f93a42a2f96841883f729aacddc4c5f829`  
		Last Modified: Thu, 15 Feb 2024 17:23:15 GMT  
		Size: 12.0 MB (12024329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe44bb7403183c92be80fb451d9b8e542668685f2e3c6e01e961c2dd8c889ef`  
		Last Modified: Thu, 15 Feb 2024 17:23:15 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faf14c4bb9e1451dc768245d9a6c7506d036b8fc7469afbe7bde03c6f5e5d91`  
		Last Modified: Thu, 15 Feb 2024 18:25:23 GMT  
		Size: 31.5 MB (31534139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5549079b477ec79b7a7d4fde4ff6c2aa0fb7d15d9abe5a39c4c51a229d9c5b9e`  
		Last Modified: Thu, 15 Feb 2024 18:25:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dab6e41063fac05359e717e21c6997125d72ab17d5c5aa7579af3dd692b0a6`  
		Last Modified: Fri, 16 Feb 2024 20:31:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e09b35aab8824815983ba50bef10489a80cc044c4ed9a5147eb8633c2c2e8c`  
		Last Modified: Fri, 16 Feb 2024 20:31:13 GMT  
		Size: 117.7 MB (117738532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7bc0ec2cf547dbad5bfc4bd04b7f7c4955a9c3624c1503eaade9e64156504d`  
		Last Modified: Fri, 16 Feb 2024 20:31:11 GMT  
		Size: 1.1 MB (1117550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3110230b3c79c2e0bd1ba84270c7fdda7808bbf42427116942f4bbfce296ae7`  
		Last Modified: Fri, 16 Feb 2024 20:31:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06be244263929cc28b90b97ab444b9dc15a02c955c830667ccc99d1c8e85c57b`  
		Last Modified: Fri, 16 Feb 2024 20:31:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9922781e35bbb1c3cdfd4590318b75df709bec486a2cbb5658460fad4ed450`  
		Last Modified: Tue, 05 Mar 2024 00:57:25 GMT  
		Size: 3.2 MB (3240627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a557b6afb9ba04e13233ac75c79a8c2cd187fe46699ef559e4f01ea90b915dc`  
		Last Modified: Tue, 05 Mar 2024 00:57:26 GMT  
		Size: 64.7 MB (64674213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947880c3840267ccf7ecce279716c4a12650d9b83287e0f717017b99d8d3966d`  
		Last Modified: Tue, 05 Mar 2024 00:57:25 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:b1c4e06d07f1d4bf133f399b50c6da5a69020ac50cec7043c6a981012b0fee3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8886695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19182b9e6b0664f441f1e3faf270a07b606e3b0d5de1919253d3b0e1da6753d8`

```dockerfile
```

-	Layers:
	-	`sha256:afd17496a905427a1136af0772007be196f3a405ea55391b75576d91deb08dfb`  
		Last Modified: Tue, 05 Mar 2024 00:57:24 GMT  
		Size: 8.8 MB (8844559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9817a18a3f67fc3818555ecd7877803c53e08234634214d39c36956cb3180242`  
		Last Modified: Tue, 05 Mar 2024 00:57:24 GMT  
		Size: 42.1 KB (42136 bytes)  
		MIME: application/vnd.in-toto+json
