## `redmine:trixie`

```console
$ docker pull redmine@sha256:1e0ba4deb15257d54ee0190492e868478b3fc50550f88ae606ea7b7ea145bcfb
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
$ docker pull redmine@sha256:1155c267e5e3c8636f3cc145d8338ee1af2b9260f7d9bfdacc5a1d55210f1491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255374846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deffcb18256fbb15375e61b3da463d74472a633c30061113ffadad70315420d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 19:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 19:56:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 19:58:17 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 19:58:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 19:58:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 19:58:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 19:58:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 19:58:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 19:58:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 19:58:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 19:58:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 19:58:17 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 20:03:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 20:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:03:55 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 20:03:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 20:03:55 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 20:03:55 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 20:03:55 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 20:03:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 20:03:55 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 20:03:55 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 20:03:55 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 20:03:55 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 20:03:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 20:04:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 20:04:40 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 20:04:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 20:04:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 20:04:40 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 20:04:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7041b753aefdf4d8adc130dbf06a044d5a62bd453821b6ab884dc3ac62e9e1`  
		Last Modified: Tue, 09 Dec 2025 19:58:31 GMT  
		Size: 1.3 MB (1279365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c41cd04f9b83417438b949987706f128227808659872f5d53502f604ce1675`  
		Last Modified: Tue, 09 Dec 2025 19:58:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0b854ee90289038b85de8900746808af89ae4474445ec3317931b7e248a613`  
		Last Modified: Tue, 09 Dec 2025 19:58:37 GMT  
		Size: 42.2 MB (42192681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88afefde66ad263b0780757b9f280aff9367848688ab9298985f874ae0e859a9`  
		Last Modified: Tue, 09 Dec 2025 19:58:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c29374d99205184625a85ca6be51fb8e044247b0550e0d9e205ba173560b4a`  
		Last Modified: Tue, 09 Dec 2025 20:05:05 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac9bca320126a2fdf562eefa98ec142b8b49244993c5409aa06c9dbfafa6bd5`  
		Last Modified: Tue, 09 Dec 2025 20:05:15 GMT  
		Size: 110.1 MB (110147923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767e1d22a51f99c530b4feb7a94aae73b275553a334a7c64951e57148afabc17`  
		Last Modified: Tue, 09 Dec 2025 20:05:05 GMT  
		Size: 949.8 KB (949765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82e0a71c171688a718ce6b57507c9a5d59e6b5a08e287a416d760a8ccaf06ab`  
		Last Modified: Tue, 09 Dec 2025 20:05:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a107c1720a4d63eabd4664d35d6947f67f6806772bedbb01b8730b5f010d8af`  
		Last Modified: Tue, 09 Dec 2025 20:05:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271553965c1163ab7536a5d09ef583bd81e1181348668370e8530ead6ee86b5d`  
		Last Modified: Tue, 09 Dec 2025 20:05:05 GMT  
		Size: 4.1 MB (4139978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a453290fbb0fecb805bdbbd90081c988a8685cad817e709f0282f48f605acc`  
		Last Modified: Tue, 09 Dec 2025 20:05:12 GMT  
		Size: 66.9 MB (66884523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9aa58111f835e31127f740c64d9b1c237dac4aae885fd40fd21ecf967869ea`  
		Last Modified: Tue, 09 Dec 2025 20:05:05 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:ff264e73a6fddac82ef4401aaa851162beec86363b73ab65fa06f88e76ebff49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77c44c709fe5de9a81035e70a777597910a341734405067f218072404573dd3`

```dockerfile
```

-	Layers:
	-	`sha256:ad48aff1141864d47bf87c6fb5ca5f54eeb6a7016f93eb46bc767754f2935c9a`  
		Last Modified: Tue, 09 Dec 2025 20:50:16 GMT  
		Size: 41.3 KB (41312 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm variant v5

```console
$ docker pull redmine@sha256:090d1054fcb7206ab764718b80fc1afa5a9adb5e657eede87e4bd6bcd8d325a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260057281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e61498c51ccb0a0f1d83ce84078ec899708b91c8197a176bcc7f1e1316bc3cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 19:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 19:54:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 19:57:28 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 19:57:28 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 19:57:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 19:57:28 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 19:57:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 19:57:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 19:57:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 19:57:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 19:57:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 19:57:28 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 20:12:20 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 20:13:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:13:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 20:13:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 20:13:11 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 20:13:11 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 20:13:11 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 20:13:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 20:13:11 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 20:13:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 20:13:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 20:13:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 20:13:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 20:14:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 20:14:36 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 20:14:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 20:14:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 20:14:36 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 20:14:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2cc54eff2c950d4469a61835c3d8fa8c991227618bf39b28ab7d289d5af863`  
		Last Modified: Tue, 09 Dec 2025 19:57:44 GMT  
		Size: 1.3 MB (1263008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b9a003fabe6302dc7c39d6e0672a7db1f2daa55e0a8f3a2e9dca1d6bcecef`  
		Last Modified: Tue, 09 Dec 2025 19:57:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad22137db260d45152a37743d2895767168aca9878a49a6457ec8ebb335f777b`  
		Last Modified: Tue, 09 Dec 2025 19:57:49 GMT  
		Size: 38.0 MB (37994154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cab1ba26c3b9267d5a1c66791ab8b88ab5c73b65ee4a5a5865a0cb1951479c`  
		Last Modified: Tue, 09 Dec 2025 19:57:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b318cac75867557e2ec8ccb44bc3bbb5c421814ef2baa05f44a097ac5c87b17`  
		Last Modified: Tue, 09 Dec 2025 20:15:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62831358c7b4158242a38a2188ccb523f7f6eb0aaf21ba425d784b80aeb167d9`  
		Last Modified: Tue, 09 Dec 2025 20:15:28 GMT  
		Size: 105.9 MB (105933080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563ee053823c7e94b82a9a9348e6a45c9bfdf48f2acaa6ed2c55f866d7558ff9`  
		Last Modified: Tue, 09 Dec 2025 20:15:06 GMT  
		Size: 919.4 KB (919407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257b25c559520776491cbddf1ffe600375685f96ce7635eb0340f40f7bf9e10`  
		Last Modified: Tue, 09 Dec 2025 20:15:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc8fee58efe685b0fe448f5f15c46848fd20545c77f7a5dbfb0ab3585104aa0`  
		Last Modified: Tue, 09 Dec 2025 20:15:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca896d736c02891468b0e87553ca61aab082c5dd065e57e7fc42b50c2496df8`  
		Last Modified: Tue, 09 Dec 2025 20:15:06 GMT  
		Size: 4.1 MB (4139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632a922cfab547e2f0e495eb92c5fd7ea9c84f831cbc9b1af919d7664c74e9bc`  
		Last Modified: Tue, 09 Dec 2025 20:15:19 GMT  
		Size: 81.9 MB (81859347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e347db02cd6e2274e18c02b1bfb6f8983abfbdfe1966ac71a2b50cbe2ee2825`  
		Last Modified: Tue, 09 Dec 2025 20:15:06 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:742229168498957851ea47ee84c3a465235c8e61326575b91283e1c02df2e01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead8c4a39d31b1d54ca7ec2efbc8ea3b550d0ae10464d040771d0df4d016df4d`

```dockerfile
```

-	Layers:
	-	`sha256:005a52fa56df6d41d573f66c05e2904dd326bf941b5b424dd46dddeff60333e6`  
		Last Modified: Tue, 09 Dec 2025 23:52:18 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm variant v7

```console
$ docker pull redmine@sha256:f124b0c062406b0fd9d5783e1b355cbc749d7166fd691127402443c9a7658144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252935566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1e924cabf0438666a5ba315d8b6f69074db5e1198448f6b353ec7abeb1216`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 19:59:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 19:59:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:02:40 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:02:40 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 20:02:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 20:02:40 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 20:02:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:02:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:02:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:02:40 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 20:09:54 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:10:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 20:10:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 20:10:35 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 20:10:35 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 20:10:35 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 20:10:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 20:10:35 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 20:10:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 20:10:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 20:10:35 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 20:10:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 20:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 20:11:49 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 20:11:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 20:11:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 20:11:49 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 20:11:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148f3a9ce86664c20486da5a2e386d42a075b2458148083575dc1a69026039c`  
		Last Modified: Tue, 09 Dec 2025 20:02:56 GMT  
		Size: 1.2 MB (1236557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811d3c1cec1c8e59a9ad9ebe5c036ec0b87eb24b175fe37b3de92c40ddba04ed`  
		Last Modified: Tue, 09 Dec 2025 20:02:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272e5dfc4820f8715e9ebf27b38fcdf51a27cf577df90e5c004e11e7fe6ba1ec`  
		Last Modified: Tue, 09 Dec 2025 20:03:02 GMT  
		Size: 37.9 MB (37865231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c0d71fcb143e06ca25d9c5d387dbff1aad7af8253501a24d26f679abc489f0`  
		Last Modified: Tue, 09 Dec 2025 20:02:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4254a559894dbcd182cdf15d6241bcc1b484764b52db1ed959d29a3bcac463`  
		Last Modified: Tue, 09 Dec 2025 20:12:12 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa881bf2b540dd2f0488be0c81195e03de9af1310fc5e2a316577cad7db4bc61`  
		Last Modified: Tue, 09 Dec 2025 20:12:25 GMT  
		Size: 100.8 MB (100843766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4a8408e08609299e1eed61ec4bc76d808b296f98af12befb3c49f33a14d0f`  
		Last Modified: Tue, 09 Dec 2025 20:12:12 GMT  
		Size: 915.3 KB (915265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e34351fe1cf1d07283033e446541225984d20c74417c866beb3005983fd59`  
		Last Modified: Tue, 09 Dec 2025 20:12:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27e324451ca0d44825398425b51c5d7d404d63fb0c2f6a73629664cdeb1534a`  
		Last Modified: Tue, 09 Dec 2025 20:12:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f99e51d7ed04b59c6f7e0654c8e4e7da8fcf91cf3ee08f180c8ac44f78bd1dd`  
		Last Modified: Tue, 09 Dec 2025 20:12:13 GMT  
		Size: 4.1 MB (4139983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8dccfc529baaed7c82cf288f32fcaa930254f9240652922135becd32f71a8`  
		Last Modified: Tue, 09 Dec 2025 20:12:23 GMT  
		Size: 81.7 MB (81720640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf3b72adc059bc89da80064911ca4d247ce70aa12398580ac8a2cbb7c08c10a`  
		Last Modified: Tue, 09 Dec 2025 20:12:12 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:c35a11ec0b3c24f6ed3013f2640d4b28483a3ae40b2a0b1cd8d0717152577b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494910eea1c1563cfdbd543c0eb5e2b1f3289b187ca6e075edabd91dc8671f1f`

```dockerfile
```

-	Layers:
	-	`sha256:09a4e5d7adda84b4fed24a381ce294bd7f3221bcc167ac720e5845361ffef85d`  
		Last Modified: Tue, 09 Dec 2025 23:52:21 GMT  
		Size: 41.5 KB (41488 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:6c3c733be936101de7f6eb6146aff35db4f0feaddca2e3e6eaa3d30438e5b130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253964432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f785631968686973bb378eaa05b8999504df7b1e0a765687ada50e48b76d3dc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 19:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 19:55:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 19:57:45 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 19:57:45 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 19:57:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 19:57:45 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 19:57:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 19:57:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 19:57:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 19:57:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 19:57:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 19:57:45 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 20:03:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 20:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:03:56 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 20:03:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 20:03:56 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 20:03:56 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 20:03:56 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 20:03:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 20:03:56 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 20:03:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 20:03:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 20:03:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 20:03:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 20:04:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 20:04:38 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 20:04:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 20:04:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 20:04:38 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 20:04:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5533416f9fb4428bbb03befb299bef0f57e3a6e5fab55a126cdb5eb32c15bc`  
		Last Modified: Tue, 09 Dec 2025 19:58:02 GMT  
		Size: 1.3 MB (1261718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f8706fae3959a4f4633b77192c5f38eac0231697de7068fc4a14ce6fda8063`  
		Last Modified: Tue, 09 Dec 2025 19:58:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8801099ca7268e9c8f5bc03b40740afa5d2b5e8fdc9cdb4bcadafc056017ff7`  
		Last Modified: Tue, 09 Dec 2025 19:58:06 GMT  
		Size: 42.1 MB (42141531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75973d1c1c62ca48dabfe8f38028cfce865e3673da777400a188200eae849252`  
		Last Modified: Tue, 09 Dec 2025 19:58:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e02aa7b077b424c113e0607f0f1cca301d2e0c1da24e2db663c35a192d787`  
		Last Modified: Tue, 09 Dec 2025 20:05:01 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8132d1aee6ad01238a2121562c92ca86a5dcf449d7359a7e58e5ceb1f4b36`  
		Last Modified: Tue, 09 Dec 2025 20:05:12 GMT  
		Size: 108.6 MB (108559511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18bea743e90eea1a2dab456fe61078a74d31ee7b5e017cf19ddff20967321c`  
		Last Modified: Tue, 09 Dec 2025 20:05:01 GMT  
		Size: 903.1 KB (903061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddeed0b84474fc128f0967891075cc06b42ab7460cce784888e0f0e4f3b3414`  
		Last Modified: Tue, 09 Dec 2025 20:05:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbba9baececb8545ed0e95eae2b9d00ee00c16858adb8ff05a2ab8067a08b580`  
		Last Modified: Tue, 09 Dec 2025 20:11:21 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb26306658f36ea98ad7fc90f0435586d3e8175dbd7e28ba874067bca6dcaee`  
		Last Modified: Tue, 09 Dec 2025 20:05:02 GMT  
		Size: 4.1 MB (4139978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645274eaf0914ebd5d754665d395cc6da1aabcb0534503652aa165ceb7479820`  
		Last Modified: Tue, 09 Dec 2025 20:05:17 GMT  
		Size: 66.8 MB (66815890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d6f54e4fe8f7bb9386c45fb7a8a78af5906277791d7cbbb3adf86371e7d3cc`  
		Last Modified: Tue, 09 Dec 2025 20:05:01 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:13627c108901b42f3d6405860e7906ae4e2cf5a19c6f657aee29fe799840ae36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca4e6e59d21c0241d3f687484aeb008b622ff5b6c95fb2757d4408e9035747`

```dockerfile
```

-	Layers:
	-	`sha256:89c8a7ae58df2ecb200e66e97fa53d9aa31f62e9b0e3ecefa98ca7c3dc4b9c48`  
		Last Modified: Tue, 09 Dec 2025 20:50:23 GMT  
		Size: 41.5 KB (41539 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; 386

```console
$ docker pull redmine@sha256:272e2f4c5a4c027ef9693d02d41e18662eeb903dd36a9a0a273e4265790736b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272264748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c616ab40f1de87d8456aae0958f51f5b93b68a92f3369e067f7a31a7d56788`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 19:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 19:54:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 19:57:27 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 19:57:27 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 19:57:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 19:57:27 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 19:57:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 19:57:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 19:57:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 19:57:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 19:57:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 19:57:27 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 20:03:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 20:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:04:24 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 20:04:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 20:04:24 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 20:04:24 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 20:04:24 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 20:04:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 20:04:25 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 20:04:25 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 20:04:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 20:04:25 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 20:04:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 20:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 20:05:45 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 20:05:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 20:05:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 20:05:45 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 20:05:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce17973ae7009b26646ad16c225f956f28fd743e422d07d47d94bcdd9d3a87d7`  
		Last Modified: Tue, 09 Dec 2025 19:57:42 GMT  
		Size: 1.3 MB (1287220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2164c592d8129a8d3aec7ee9cc6f82883cf652e4ef710b9346dbe16f86eaa3`  
		Last Modified: Tue, 09 Dec 2025 19:57:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6e558dac196b8d8a488abea2076a3d879f1e86709c11217eb060f292891322`  
		Last Modified: Tue, 09 Dec 2025 19:57:46 GMT  
		Size: 37.7 MB (37739957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f060bed064d65789ccaa123bf15e1dae11c563e69e1bd3455a28155305610f45`  
		Last Modified: Tue, 09 Dec 2025 19:57:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734863c8535faf825462fbb7be02dae81337d184fdfc9f6e5f9a10fcd1ba3da5`  
		Last Modified: Tue, 09 Dec 2025 20:06:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb961edd4dbbd724bd18103c047c9df8cf7d3e11187555293a8d4d47ab4ab52`  
		Last Modified: Tue, 09 Dec 2025 20:06:29 GMT  
		Size: 112.7 MB (112659310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e842edfb928628455aade06e7137f3d0f10216ebc022ec81f14c3d18a4c17b6f`  
		Last Modified: Tue, 09 Dec 2025 20:06:08 GMT  
		Size: 918.6 KB (918595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf31078db4e5f0cbc43ead6489869f331c22cf7d457c11d20a36c2d18f660f8`  
		Last Modified: Tue, 09 Dec 2025 20:06:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c2ba89df9f9d3dc417c3f9ec91dff7ef53216b2d0410639b94bf2efca3af5d`  
		Last Modified: Tue, 09 Dec 2025 20:06:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9738929745c251aa397f859f0dcf69ac5a3a0fd1a2524af5051f2b66ea7158`  
		Last Modified: Tue, 09 Dec 2025 20:06:08 GMT  
		Size: 4.1 MB (4139982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48f4f00a0e7868a8e7f07a901aba9f8d574fc53cee8e03999cc5a354ab27276`  
		Last Modified: Tue, 09 Dec 2025 20:06:18 GMT  
		Size: 84.2 MB (84222500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0baa3c603234e312ec0bcc6bedc7e99816bca95416326e73681893638df86`  
		Last Modified: Tue, 09 Dec 2025 20:06:08 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:100caa8ebfe5c6dd8329fbb6c142069b1ffcad8a9fc1e1aaf431fa621c49d123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b12e9ee93b4c0ef6d8b29438f20eadacf2f2a782b81438dc41711cdcd33353`

```dockerfile
```

-	Layers:
	-	`sha256:ad2b9164cf0ec6d5fe20f0dd2268b5adf0b55aedc012d0cb7ddbaeba72115179`  
		Last Modified: Tue, 09 Dec 2025 20:50:27 GMT  
		Size: 41.2 KB (41250 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; ppc64le

```console
$ docker pull redmine@sha256:c3be5000e269c0fb6dd89d001359feceb7009777dd25986b321f3ddba9f126e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295754742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea279ea2c9b19fd3aed7636466b988b032093d24ca9135df8d6ff1a8c75925a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:34:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:12:19 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:12:19 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 20:12:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 20:12:19 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 20:12:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:12:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:12:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:12:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:12:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:12:19 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 21:15:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 21:17:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 21:17:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 21:17:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 21:17:49 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 21:17:49 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 21:17:49 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 21:17:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 21:17:50 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 21:17:50 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 21:17:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 21:17:50 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 21:17:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 21:22:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 21:22:31 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 21:22:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 21:22:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 21:22:31 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 21:22:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d3671620f3e48336d62a7594d5e2d543d9e64a95aad33bfc1d7771e56acf03`  
		Last Modified: Tue, 09 Dec 2025 03:40:15 GMT  
		Size: 1.3 MB (1309685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f018d664c90820e92e1c9763e0ff1c2d9fac0edb7ffc1e2324b238098d157eac`  
		Last Modified: Tue, 09 Dec 2025 03:40:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47658f0b3cc64e1f3f28104145e05591821438ffbae83e8320199d5aee0922`  
		Last Modified: Tue, 09 Dec 2025 20:12:48 GMT  
		Size: 39.6 MB (39616785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb155eef6c56eebf52b44f03ccb19dbfe894fd695ea01babbe939dcd30d484e`  
		Last Modified: Tue, 09 Dec 2025 20:12:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f88c197cd311427f3f468ba38e61c61c1f020ce85aa9c79e40823ccc2623123`  
		Last Modified: Tue, 09 Dec 2025 21:23:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8ad5c5680532bd700442da97923a61ba567a36ed3428814ad46266b62bc926`  
		Last Modified: Tue, 09 Dec 2025 21:23:42 GMT  
		Size: 117.6 MB (117624942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e5b1e564bbd63520a2f5865ca9afa4f197ac84f6b817a3c088d958f3e42eb`  
		Last Modified: Tue, 09 Dec 2025 21:23:34 GMT  
		Size: 909.4 KB (909401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0febdad3ae270d367eba85d284103a36eb93b95133033077f06694c677202615`  
		Last Modified: Tue, 09 Dec 2025 21:23:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a46b8f4b174ca757956f55ea0c6eff22cb89a52e57162838cb23f510c6e98aa`  
		Last Modified: Tue, 09 Dec 2025 21:23:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ad9bf2deee1961fcf90c45272fa8f6f1e794a1b968ff3ce0a8ff42de2160eb`  
		Last Modified: Tue, 09 Dec 2025 21:23:34 GMT  
		Size: 4.1 MB (4139976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7557409a1e682c93569629833f4292cd17ccf76af8dde1a1d9598a5a57252221`  
		Last Modified: Tue, 09 Dec 2025 21:23:43 GMT  
		Size: 98.6 MB (98552950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3d59a5fee6a332058ba449d765481e51c6937840d9f7fc3a7f22a0006a09be`  
		Last Modified: Tue, 09 Dec 2025 21:23:34 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:53118a8aeb0171233b56abfb9f3ed68cf3c2d8ca597d55eb77017c1eab7b735e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a42cab306f5dfc97bb95a9eedee772abb2a8e9dd8342b6e3bc1dce1b3a0081`

```dockerfile
```

-	Layers:
	-	`sha256:4f99bbfec35525491b7f991611cfbfbf6afe75231d80aa739b272ce6f33bbdd4`  
		Last Modified: Tue, 09 Dec 2025 23:52:28 GMT  
		Size: 41.4 KB (41390 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; riscv64

```console
$ docker pull redmine@sha256:ee923abf5b4d8079607d794211602e8d486eead9c96191a54cac19bc7c729ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279657045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ebe4e974e122c8ec2a6a1423d8ac41b0cf97b008ff4eb040a042ee1d2f57ee`
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
# Fri, 05 Dec 2025 19:47:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 05 Dec 2025 19:51:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Dec 2025 19:52:08 GMT
ENV GOSU_VERSION=1.19
# Fri, 05 Dec 2025 19:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Dec 2025 19:52:08 GMT
ENV RAILS_ENV=production
# Fri, 05 Dec 2025 19:52:08 GMT
WORKDIR /usr/src/redmine
# Fri, 05 Dec 2025 19:52:08 GMT
ENV HOME=/home/redmine
# Fri, 05 Dec 2025 19:52:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 05 Dec 2025 19:52:08 GMT
ENV REDMINE_VERSION=6.1.0
# Fri, 05 Dec 2025 19:52:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Fri, 05 Dec 2025 19:52:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Fri, 05 Dec 2025 19:52:08 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 05 Dec 2025 19:52:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 05 Dec 2025 20:59:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Dec 2025 20:59:49 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 05 Dec 2025 20:59:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 05 Dec 2025 20:59:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Dec 2025 20:59:50 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 05 Dec 2025 20:59:50 GMT
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
	-	`sha256:46c87cb14702e1e239913a52380c92b98c50edcb2c2ba76d541f4c538f59689a`  
		Last Modified: Fri, 05 Dec 2025 21:03:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65328670939f52f1a74aff7503a94f679c567dac021d92404019fdb5f3758a35`  
		Last Modified: Fri, 05 Dec 2025 21:03:33 GMT  
		Size: 107.4 MB (107394767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3848b0e5f3f4e6309379fc4b0cba66bef9110f0f926206aee0dfb2812734d4b8`  
		Last Modified: Fri, 05 Dec 2025 21:03:20 GMT  
		Size: 896.4 KB (896395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a6b68524ce78a5d1defdc919142ff0933fd114e551a15d45a66f1bc34ec53a`  
		Last Modified: Fri, 05 Dec 2025 21:03:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e6f2aa6488ab561d018089ce4f50c5007b04de87aa5859436ac29c86996a7c`  
		Last Modified: Fri, 05 Dec 2025 21:03:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3184ed26f0d0df50d4af0aeef3a7c95762c93f7a58ed84d4cd07567b953c70ed`  
		Last Modified: Fri, 05 Dec 2025 21:03:20 GMT  
		Size: 4.1 MB (4139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad102e450a31888b8e16661ed2c4b308145132373cb1b548e3d11f56eb69445e`  
		Last Modified: Fri, 05 Dec 2025 21:03:36 GMT  
		Size: 99.7 MB (99708790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e30eef554ea6f21ceb13ac0eb8bab3a74ae427883d1ab322c7dde1b7093a8d1`  
		Last Modified: Fri, 05 Dec 2025 21:03:20 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:1836c635ad5abe65ddaf155c10106523734735f70ebe1a272f91f1de494c4a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4d6c5fc35e42313f6713c05fe601ce7da34821107360a4411c0e3d735f6241`

```dockerfile
```

-	Layers:
	-	`sha256:87a6b38f579e1d4fcdf151c49606d23e8ab2bc59182227e58fc9397df5e21c33`  
		Last Modified: Fri, 05 Dec 2025 23:51:15 GMT  
		Size: 41.4 KB (41390 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:trixie` - linux; s390x

```console
$ docker pull redmine@sha256:3052889a11dc364d3ffd52c07f8efdb9177db0142f5b1569a106605f52a9cecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283611278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a433302a37834224d872d75887f04f70a3aa545591ce5c6fc448595f8cb832`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:14:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:00:34 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:00:34 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 20:00:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 20:00:34 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 20:00:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:00:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:00:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:00:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:00:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:00:34 GMT
CMD ["irb"]
# Tue, 09 Dec 2025 20:17:15 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 09 Dec 2025 20:17:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:17:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 20:17:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 20:17:58 GMT
ENV RAILS_ENV=production
# Tue, 09 Dec 2025 20:17:58 GMT
WORKDIR /usr/src/redmine
# Tue, 09 Dec 2025 20:17:58 GMT
ENV HOME=/home/redmine
# Tue, 09 Dec 2025 20:17:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 09 Dec 2025 20:17:58 GMT
ENV REDMINE_VERSION=6.1.0
# Tue, 09 Dec 2025 20:17:58 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Tue, 09 Dec 2025 20:17:58 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Tue, 09 Dec 2025 20:17:58 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 09 Dec 2025 20:18:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 09 Dec 2025 20:20:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 20:20:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 09 Dec 2025 20:20:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 20:20:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 20:20:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 09 Dec 2025 20:20:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720eba478777df8c646e25a1f6668894f78c60729b8066bb843a45e90174380`  
		Last Modified: Tue, 09 Dec 2025 01:17:18 GMT  
		Size: 1.3 MB (1294285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32a4b1f7561f4abaafe6220c2c2f308127ee5ef35474833e833a9af097e333`  
		Last Modified: Tue, 09 Dec 2025 01:17:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae93aa653b5aad3bc62502481999438400bfb3c5dc964e6d641ae337e3b1ec1`  
		Last Modified: Tue, 09 Dec 2025 20:01:00 GMT  
		Size: 39.3 MB (39302658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154db5788acb94c793098c6aea101bdb649ab42fd2bfc6fd76ed3eb9f610a4a`  
		Last Modified: Tue, 09 Dec 2025 20:00:55 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e9fa29edef7d4a1dfdf3cc51e1f85f5af59b17c019a587a0caeb6a12551ae6`  
		Last Modified: Tue, 09 Dec 2025 20:21:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c8602c84a07f238253307a6972cbeec70163473393491e39ddd6ceb5138e92`  
		Last Modified: Tue, 09 Dec 2025 20:21:33 GMT  
		Size: 110.9 MB (110948919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e2bddf37660dde1b77e6f794e307901affacef03611cc464648a20053393ac`  
		Last Modified: Tue, 09 Dec 2025 20:21:18 GMT  
		Size: 922.4 KB (922434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eee309e12af10f0315826701bff83ebe5ea19f9651d12465e1d95efe69e0a1`  
		Last Modified: Tue, 09 Dec 2025 20:21:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09d086752a3dd80523eff2cf8d77cc111c6b77fadff269c9e7b5cc35e22f39`  
		Last Modified: Tue, 09 Dec 2025 20:21:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2f0cddbcba24f794a14294d1451d28317ab25b5584f8c4a2c1d72ea252be3a`  
		Last Modified: Tue, 09 Dec 2025 20:21:19 GMT  
		Size: 4.1 MB (4139981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979982ac15eae48b9011d2a850681774bd0ae87577a8a64404930f17256b6c1`  
		Last Modified: Tue, 09 Dec 2025 20:21:30 GMT  
		Size: 97.2 MB (97164486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d48239217f4d90eeba18c54976210c196b5ff7b6f1356a15e4c1602cfaeaae`  
		Last Modified: Tue, 09 Dec 2025 20:21:18 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:trixie` - unknown; unknown

```console
$ docker pull redmine@sha256:45bb389fde87dae9fd4c2b1f56937d66a54c09e70b6290a603f41c9fd1b748ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc5d28137710c404c2016dd71b31ec958e3f1b92a6b8c6941dbb7e39be1bfb9`

```dockerfile
```

-	Layers:
	-	`sha256:43c944cf10efd222e6b1395a5164b726f66d669cbd8d6a5069ec2c8a302e5166`  
		Last Modified: Tue, 09 Dec 2025 23:52:32 GMT  
		Size: 41.3 KB (41311 bytes)  
		MIME: application/vnd.in-toto+json
