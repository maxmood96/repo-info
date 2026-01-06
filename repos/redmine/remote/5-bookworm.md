## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:99b8a0a2bb3ae50aba875028b58013b9844e05beb0e32ef9d100fa44b640ecf0
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
$ docker pull redmine@sha256:dcb012750c688b8af9de32fb0af8d1797cea7cd7c49c7f52d24b9f9d8d2f41e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249902113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e58c7fb0dbe2fe3216b79bd8993e5d87830872c03448e6973e1eb32ae4bd6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:47:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:49:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:49:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:49:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:49:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:29:07 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:29:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:37 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:37 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:37 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:37 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:30:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:30:09 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:30:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:30:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:30:09 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:30:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc57904889217c8f0331318b3d24c3dbf235fe535edf8e2e73836b99679969`  
		Last Modified: Tue, 30 Dec 2025 00:49:39 GMT  
		Size: 3.5 MB (3509707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfab611350d463ece772d5f8dd961f0874536785bd07206733fe163ee785bfd`  
		Last Modified: Tue, 30 Dec 2025 00:49:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a1cb5318ad089abb0784ad830f80a620dd9cf88b747c91db4b20b7a949c5f`  
		Last Modified: Tue, 30 Dec 2025 00:49:43 GMT  
		Size: 36.0 MB (36008166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f971dc91a875a9ea356df935b7d977e46b610c2e84794e7b5fc1179cd4d2279`  
		Last Modified: Tue, 30 Dec 2025 00:49:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4449fa8100a0dba0a8826265ba81c724c12b61c9ad26ffa98f74a05cabcb4ffc`  
		Last Modified: Tue, 06 Jan 2026 18:30:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df003f99ba280e18a819f1dea53734e00855962ee3d0ffecca64e9ada8f067aa`  
		Last Modified: Tue, 06 Jan 2026 18:31:00 GMT  
		Size: 122.9 MB (122943091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad6e54d13f3959f71d8d981f5d770ee5c4fb62742c8c2c240d5e4b229957b04`  
		Last Modified: Tue, 06 Jan 2026 18:30:37 GMT  
		Size: 947.1 KB (947116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8318db969e8d04193629789ba1ff5cf3ff1db16a9977a4e9d4e70863944a495b`  
		Last Modified: Tue, 06 Jan 2026 18:30:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2267b6041dc32e5e97bb1ca986ea45931ea4966682e4700bb85d1a7288fab77a`  
		Last Modified: Tue, 06 Jan 2026 18:30:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f873c107e453a6dc502944fd8785d781f603ad6ba1296eaf358750ff78d990ef`  
		Last Modified: Tue, 06 Jan 2026 18:30:37 GMT  
		Size: 3.3 MB (3252910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78e9e59e00aa8e0a876c09c1ccd2e49e761b073dbc8d2e3e646700567f684a6`  
		Last Modified: Tue, 06 Jan 2026 18:30:45 GMT  
		Size: 55.0 MB (55008581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fea5562c38e56d4311585f9988cae888bb524ecdd4ae40a456468618f6a1856`  
		Last Modified: Tue, 06 Jan 2026 18:30:38 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:2d04578a0e088dfcd9a2f90d3de1f23af6bff44db700554c42e8d3b0078a2a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c412f39f4dd26d4f83994df28b27353795494bc5e12c6b0fdd5d0cbca3c884db`

```dockerfile
```

-	Layers:
	-	`sha256:ed43e218ac22aa292e8bbb5846a414cb20ee1783d0451ceb0dca9c1e94235567`  
		Last Modified: Tue, 06 Jan 2026 20:51:22 GMT  
		Size: 40.1 KB (40147 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:547ce4c485a2e320122a113c5a931045f5eecfc174b2d4caf7bc4c685a3718a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234138134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d61f7ab865caa395d297ca73f40ed694b9dfecd56dfed74ddf07a652711932`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:16:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:16:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:16:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:26:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:27:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:27:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:27:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:27:19 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:27:19 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:27:19 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:27:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:27:19 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:27:19 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:27:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:27:19 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:27:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:28:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:28:03 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:28:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:28:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:28:03 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:28:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8eb03a5eb5dc316e7d14f2cc3e1ac5fb3a475bec74d4d59bbc8009986997a`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 3.1 MB (3079815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c84cec1d2a69d1b707673854472bdb4481a2f40b9234a607f80d9a3d7a8ee7`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdded823509c9fa8e84064c1dd7d9425dbd644062010544cabe1d7cfb8b6477`  
		Last Modified: Tue, 30 Dec 2025 01:16:59 GMT  
		Size: 32.3 MB (32327459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f8ae75d3527b4ff18a47a14ae5014ef580ce159702b603a52e1db6d1f77393`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7def1ac5ff80c2154edcd3e98cc0e6e9d69f1e1d93bb3f5671924ce6aeaabccf`  
		Last Modified: Tue, 06 Jan 2026 18:28:29 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e411d4c8bef4a68b09e1781c967864ff5de265622a6736825c126a963e37dc`  
		Last Modified: Tue, 06 Jan 2026 18:28:41 GMT  
		Size: 116.6 MB (116617576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974f7e7211a632609b58626976e3e677004ae07bc5e77bec3a407fbd3f0ae2be`  
		Last Modified: Tue, 06 Jan 2026 18:28:29 GMT  
		Size: 916.8 KB (916763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49f5e77fdc8ccf79d1b8c6a4c014c1d97432bb92f93ab3f1472086ee4bd0532`  
		Last Modified: Tue, 06 Jan 2026 18:28:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898e74e4a716efc11e460519b2b54797d6f709c3ea10e6c5d6045bf414c4293`  
		Last Modified: Tue, 06 Jan 2026 18:28:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2446be3b9b8f513dcf2a2f6739239a3cf29705583471a5faadcaaef80c5fff73`  
		Last Modified: Tue, 06 Jan 2026 18:28:32 GMT  
		Size: 3.3 MB (3252916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be51377b2f0e08001733779e76e43584e1ebbdd955b12d18ba418b46e65edfae`  
		Last Modified: Tue, 06 Jan 2026 18:28:35 GMT  
		Size: 52.2 MB (52181912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692bcb9e318ded8836263535fc5a66a496a87af3f71604d2480fd2fb5e78eea`  
		Last Modified: Tue, 06 Jan 2026 18:28:29 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:6d70954eeec9fe6c2343266052f4298382205181b0033efafd90e80ac39371b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44c4e1e6bdeba3c5bf41ddba1118231168b67d9b1a8a61c5872d90758529900`

```dockerfile
```

-	Layers:
	-	`sha256:57780d81f71a0160451c01a05d71be7bf82343391b857b3c2ab44a07882342fd`  
		Last Modified: Tue, 06 Jan 2026 20:51:26 GMT  
		Size: 40.3 KB (40284 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:50c99fe7706f0287de3cbbab53fdfc21c0721ed7bff87809dde2b577d278002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227213687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7837ca429eeb7c6b7f635a8ec9ba860a582e8c27f8968b894bf70993430fcde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:47:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:47:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:47:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:47:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:28:51 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:29:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:28 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:28 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:28 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:28 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:30:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:30:07 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:30:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:30:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:30:07 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:30:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7b5dece593c8cbb29a37091a49cbcd13486bd61cd33d3ab360b403b7b84de3`  
		Last Modified: Tue, 30 Dec 2025 01:47:33 GMT  
		Size: 2.9 MB (2912747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb97ce5a95c82339bebf579a8181ce972cd84f66f1b06d8c58c0c3f25f32593`  
		Last Modified: Tue, 30 Dec 2025 01:47:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2131befd86e0cb6e898d6f2e1e3b2c38aab4e8e726f3944131b4c9b670fa67b`  
		Last Modified: Tue, 30 Dec 2025 01:47:34 GMT  
		Size: 32.2 MB (32161925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fdb606e7417b70421caa2627077ce7ccf1fc46a69aab2805b8baa4930b6df5`  
		Last Modified: Tue, 30 Dec 2025 01:47:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccc87059f83c79a7f73d132abc281fe350a5f48a0056d5910a870d5753c07c4`  
		Last Modified: Tue, 06 Jan 2026 18:30:30 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22388e21ee1f09d91d352481d46c4be09da98bd7020ab74f061e56d7be6e99b0`  
		Last Modified: Tue, 06 Jan 2026 18:30:45 GMT  
		Size: 112.0 MB (112004800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b3549d75c9590e63b22df79a5c360716f377ba2930c2d88ea0848afa835ef4`  
		Last Modified: Tue, 06 Jan 2026 18:30:31 GMT  
		Size: 912.4 KB (912355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d79b03f10bb8893e9063565d784a1d4a1503b5c16a63b6ea912aeb50ed71`  
		Last Modified: Tue, 06 Jan 2026 18:30:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988e39166255c68deb726a60c4dbb849095bb06d102f2bd3eb19644a6ea91c26`  
		Last Modified: Tue, 06 Jan 2026 18:30:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738d7c023779ea0943e2fd39bda33542434ce46fbec57aef5fe07c0c6ef99c62`  
		Last Modified: Tue, 06 Jan 2026 18:30:31 GMT  
		Size: 3.3 MB (3252913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c050974bfe5f3fdaf0893dda842c8cad83df57aa73a7d41c988f8af2ba4baeb`  
		Last Modified: Tue, 06 Jan 2026 18:30:38 GMT  
		Size: 52.0 MB (52030778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27d21ba64109abb9c5b92d8e042070c1b381e089d50716a0bacad325c700c4`  
		Last Modified: Tue, 06 Jan 2026 18:30:31 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:56411f41046a6ccb2a74b94efb547c36cc4e08e422dbfaf2e5675f92935b621f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbd844693a3f827daa4a717ba4af340b49fed1024f06f6e565441ae9aea87e4`

```dockerfile
```

-	Layers:
	-	`sha256:cd12ae9e32ee68a1559d4750f9fd4c86e8c6aed2a19b8c96d5e4be4881912066`  
		Last Modified: Tue, 06 Jan 2026 20:51:28 GMT  
		Size: 40.3 KB (40284 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:64bf63e3d068f3045cfb9e56990efb31b16f75b8683bc294777ceaa37caad53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246204395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2f97f455770944ad1b6cf16ffe40d8a980619e0211774729cf3a2e84f0e8d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:50:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:52:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:52:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:29:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:29:55 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:55 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:55 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:55 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:55 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:55 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:55 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:55 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:30:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:30:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:30:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:30:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:30:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:30:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae7c40900658b18d348bd2774604c46eca98d08ef1d45a1f985d0cbc1f4e5c6`  
		Last Modified: Tue, 30 Dec 2025 00:52:46 GMT  
		Size: 3.3 MB (3340664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f8d350e700bb8acd50f81d0a28cf15ef5b70d1c463bb7b91bd43220a39cc54`  
		Last Modified: Tue, 30 Dec 2025 00:52:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5617bc1baec7c56f0156f71e4e51a4864979dc850b678067e8d32ba855785a6c`  
		Last Modified: Tue, 30 Dec 2025 00:52:49 GMT  
		Size: 35.9 MB (35908942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dad51bbc72b51dc192dd58ed0f2cf9fa9cfc24d438b54790831864a1a607307`  
		Last Modified: Tue, 30 Dec 2025 00:52:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f215e51f721b7af41fedccab22b495674381dfaffc86a28f25b78e422aeb2b73`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f440e892871aff80bd55d0023fe2968d6510114cbd37e1f32d888ec515c5444a`  
		Last Modified: Tue, 06 Jan 2026 18:31:10 GMT  
		Size: 120.3 MB (120307490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760aa873066727381c2ce84a2c91a74875f716b469b8801b94fc09052e162e9b`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 900.7 KB (900731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f3cf7b088b8838e2c112a8bd551031dda15896e421aaef5cc60fcc760975e4`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9717d4876c31d025f709440e99dbe8d20603f29ec4630920f695cfd3774acd6a`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1746e6a11b0b57c9ccdf2233df041a697ba66ffb955c840b096272145437a48`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 3.3 MB (3252910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283228b12cbb91e257b97bef1df29b03c5cc83b1f4e4cc090e2ec68be7363e7c`  
		Last Modified: Tue, 06 Jan 2026 18:30:58 GMT  
		Size: 54.4 MB (54387329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea106b26745cb1c60b6dd5822c1ff0406512c71c95326ff7edee5ab2527f73e`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:0a8d3ccfb1e8c525353c51e61805697521f4b41575bf3333ac0acd93626c7f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2124fe8bc3af958b09b767c2173a0ac272b06b8628b3a2ee07ab7f5a0d5576`

```dockerfile
```

-	Layers:
	-	`sha256:9edb831d883b6703f5bea2f649a25c6bbb47a0e723d05649aaba302ec64b7cbd`  
		Last Modified: Tue, 06 Jan 2026 20:51:32 GMT  
		Size: 40.3 KB (40313 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:d4a0a0f55ff0da7e1a2a93915db6c17ccc49e3d35da8f271a015a90b23899af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248170909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a83b723f0feb02f07a65f9c871298f124130d66c66a572a6a2937d71a325469`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:17:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:17:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:17:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:17:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:27:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:28:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:28:16 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:28:16 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:28:16 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:28:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:28:17 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:28:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:28:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:28:17 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:28:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:29:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:29:01 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:29:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:29:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:29:01 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:29:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fbd368b46ddd6b63ad9ce6cee84be7b9ba182a72c7e222c298e3d8fcef7ebe`  
		Last Modified: Tue, 30 Dec 2025 00:17:20 GMT  
		Size: 3.5 MB (3510976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a03bd78cba1c0c4f9c767a5eb56c26010280a0812c10086c90f2836d0e0c21`  
		Last Modified: Tue, 30 Dec 2025 00:17:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855343f9fd97a631f9bcdb6cd5501b87a86b6ae39eb3c6ea6cbe92bdbf6d6ccc`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 32.2 MB (32160077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700247d907b673a939c55b9bc927d13dcfb318b76b7d7b3b4b546f0cc721bdfe`  
		Last Modified: Tue, 30 Dec 2025 00:17:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2719746e786eea017c1ed2382c3073bfa24c83acb3147903573da7de848a19d0`  
		Last Modified: Tue, 06 Jan 2026 18:29:28 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8f9482661dfb2d4e3a9618155caadadf7e0e8e28015fc4b76aa83c0a8819b`  
		Last Modified: Tue, 06 Jan 2026 18:29:35 GMT  
		Size: 124.8 MB (124810018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866d8ff7318d2322a245e6acf7ed6f946f723d54ac81027f146dbb9a20b1b866`  
		Last Modified: Tue, 06 Jan 2026 18:29:28 GMT  
		Size: 915.7 KB (915701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb5d9328b1550244793d881ac9bc2017f0ec0cd80979c299db82379d3a84994`  
		Last Modified: Tue, 06 Jan 2026 18:29:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ce7c7d962caf04401528539c18e0a64e3029ed7ca4f75e87fa0e6a86a5133`  
		Last Modified: Tue, 06 Jan 2026 18:29:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e28e4311e6d9df35d0b2b61a14d1e1708c902b9a9f37d89977bc1496db4ac0`  
		Last Modified: Tue, 06 Jan 2026 18:29:28 GMT  
		Size: 3.3 MB (3252914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e3f7e952cf109f5143bba860e9c9e817dc43e38b1e65386f09721474be2cf7`  
		Last Modified: Tue, 06 Jan 2026 18:29:34 GMT  
		Size: 54.3 MB (54307333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172679e9c1d466bf5a5fb94bae9e93d0764591c38046cee69a32bc29a1772dff`  
		Last Modified: Tue, 06 Jan 2026 18:29:28 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:dc6270320688259ac02676f0c8651efe7d411f0cc6f0a615da8d26b30b88d774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d3a59698278d03c0610dccbfadc307732ecfd4b6812e69c6370c7ea97d12c`

```dockerfile
```

-	Layers:
	-	`sha256:4aa3054b0592cabc04f9565bfbc1851df85f1608f6bf1cfe73701c9688a68326`  
		Last Modified: Tue, 06 Jan 2026 20:51:35 GMT  
		Size: 40.1 KB (40110 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:21e48edd9e0e834768dc030672c7b3e71e6479e483214bb12d190066cdc19e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253791015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991b779cfe785f3c0339d7760d515481447e5a7613e90b463b55c9a068eb1b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 16:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 16:06:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 17:10:10 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 17:10:10 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 17:10:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 17:10:10 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 17:10:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 17:10:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 17:10:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 17:10:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 17:10:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 17:10:12 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 18:28:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 30 Dec 2025 18:31:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 18:32:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 18:32:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 18:32:05 GMT
ENV RAILS_ENV=production
# Tue, 30 Dec 2025 18:32:06 GMT
WORKDIR /usr/src/redmine
# Tue, 30 Dec 2025 18:32:06 GMT
ENV HOME=/home/redmine
# Tue, 30 Dec 2025 18:32:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 30 Dec 2025 18:32:08 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 30 Dec 2025 18:32:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 30 Dec 2025 18:32:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 30 Dec 2025 18:32:08 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:37:21 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:47:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:47:09 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:47:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:47:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:47:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab807473bbd7ea292a64937a2aec3b89f0de88151f46993597cdfe1631881a7`  
		Last Modified: Tue, 30 Dec 2025 16:23:32 GMT  
		Size: 2.9 MB (2900472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc319412b18b83e65d9dad43ffbee67efb6391dbae86d19f046079ff95a1e21`  
		Last Modified: Tue, 30 Dec 2025 16:23:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c29818667ea282c2b39c10693c96e557a3e29d8bc951129642830b703ab0ea3`  
		Last Modified: Tue, 30 Dec 2025 17:10:58 GMT  
		Size: 33.4 MB (33351924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3549fd1a0b34a760f7eb02e270732fe8f8203b3c5b470faa8e8d8f35eeb5e699`  
		Last Modified: Tue, 30 Dec 2025 17:10:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320cf6daa4d03fa7c630d9975a90944fabdedb99f39c4c124c3e8b318e4ffd84`  
		Last Modified: Tue, 30 Dec 2025 18:45:20 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e5a1158cbe62275c2dbedbd938b74288d30abc870329a2d7637fb59be65453`  
		Last Modified: Tue, 30 Dec 2025 18:45:36 GMT  
		Size: 118.5 MB (118450871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4ce13f6cc79da983d7a25e0885f45f80de5567b50a561c383cb8d29468ed2`  
		Last Modified: Tue, 30 Dec 2025 18:45:20 GMT  
		Size: 857.2 KB (857189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c56ede0362a305b283680a2a47b1ab1f699544b5f21c38724bde85c8e3e46d`  
		Last Modified: Tue, 30 Dec 2025 18:45:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee753469c016963c5353c076f93208244ba98ac57fe1fe08086942687b6b3c8c`  
		Last Modified: Tue, 30 Dec 2025 18:45:20 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b6f36868d0955b4b2ec91647934ef5705c1bb5650289ebc9c1fcf5b5cf7bcd`  
		Last Modified: Tue, 06 Jan 2026 18:48:40 GMT  
		Size: 3.3 MB (3252921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f40a4f35947ac39dee5946c8605b983142dfeab3debdef251281fa658a298be`  
		Last Modified: Tue, 06 Jan 2026 18:48:46 GMT  
		Size: 66.5 MB (66459711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76585016b37cfc8e35a2d6380a463ac31237aa9fed8a046a88be8e5fcc3d3405`  
		Last Modified: Tue, 06 Jan 2026 18:48:40 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:d73afc7dd926f1db7dbf91b96d92dbf8c12a547bb6eb0729fb0bc3d79f171027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a27261b089a18d0f11571a15bcb32da0abc435a6ea960e5dff701f34c2e34d`

```dockerfile
```

-	Layers:
	-	`sha256:dde70c4e283e372e2096c9d0baedb53f7c6bf17aaea04316ddf22e4c0780ccbe`  
		Last Modified: Tue, 06 Jan 2026 20:51:38 GMT  
		Size: 40.2 KB (40219 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:18b6a1a298351c5b90c02cfc252cae968d9ed305a21168378d5251cd99291533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.0 MB (270974861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55b59c505379640a46ca0c986799c3358bbfd2437a49d4e106e36fdc079c6c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 04:57:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:57:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 05:11:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 05:11:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 05:11:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:11:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:47:28 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:49:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:49:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:49:04 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:49:04 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:49:04 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:49:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:49:05 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:49:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:49:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:49:05 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:49:08 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:52:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:52:35 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:52:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:52:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:52:36 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:52:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9cebfd28c842195ef306457f689bf8cbec529ccf65729ab7749cf1505623f`  
		Last Modified: Tue, 30 Dec 2025 05:02:13 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333055b244abc340531d6bf67be5e762ede7cc94d700c3a3bd170892ea00113`  
		Last Modified: Tue, 30 Dec 2025 05:02:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386747298c411ef446c44b05925fcca2e6ee47e039f8608eb84ce4428a5c9d5`  
		Last Modified: Tue, 30 Dec 2025 05:12:18 GMT  
		Size: 33.8 MB (33832992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d894c7df1e0acbf3b7cbc7f42df580787a6cc196eb3535767a153975936125`  
		Last Modified: Tue, 30 Dec 2025 05:12:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72ece753bd1ad1740cd3537e53ed65a67fcd78651f5a9ccf7db9d647534eea5`  
		Last Modified: Tue, 06 Jan 2026 18:53:22 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9361249e86c827e8ab2d342564f71596ab84fd8e96b6c26f9d353452d76095`  
		Last Modified: Tue, 06 Jan 2026 18:53:56 GMT  
		Size: 129.9 MB (129933339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d7bef8faeb50814da233489cacacf65c24d246c88f6993bb05a6c169404192`  
		Last Modified: Tue, 06 Jan 2026 18:53:22 GMT  
		Size: 906.8 KB (906754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3f299f67b736120393978f58a27ccff479635f7eadb9b0179c3370d1a01825`  
		Last Modified: Tue, 06 Jan 2026 18:53:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac004896fa2e7eccbcacbc1a62d37608ca0a09deea805952f5690b460a3f2ded`  
		Last Modified: Tue, 06 Jan 2026 18:53:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8e09d2efd42cf07c1ac33c63c9ff858c24746973257cfae271ef723630c23`  
		Last Modified: Tue, 06 Jan 2026 18:53:24 GMT  
		Size: 3.3 MB (3252907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a41f367e7c4b31a5373a0e698f8c7f6a841c73eff2965d6dd9012811891cc`  
		Last Modified: Tue, 06 Jan 2026 18:53:31 GMT  
		Size: 67.3 MB (67266842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320e92fbc083e4578a969ce3b040cb5dca75f6f5556febb629a825a563d6fd38`  
		Last Modified: Tue, 06 Jan 2026 18:53:23 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:7e2bfce87fea6ce8db63b727b481161ca5e483b4eb0b5819148724f33b6b1e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ae11e21e2264522a16824e6bf1384a42dc8b33d11a8316145050bd87e7930`

```dockerfile
```

-	Layers:
	-	`sha256:9e5755a9a5937b3e26bf31548c35f287ffaa7a70fe0b1e876e91ce9a3c4c5871`  
		Last Modified: Tue, 06 Jan 2026 20:51:41 GMT  
		Size: 40.2 KB (40195 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:0c897834809f6833b4ea616ff223ffc929ea9ed171ba7ab3b8650febc31ee30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251291438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bfd4358836a71b31ec8fa22ece48042f15ddc0c7129325fb7a7f15de6ca80d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:51:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:59:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:59:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:59:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:59:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:32:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 18:32:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:39 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:32:39 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:32:39 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:32:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:32:39 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:32:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:32:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:32:39 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:32:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:34:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 06 Jan 2026 18:34:37 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:34:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:34:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:34:37 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:34:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45ef165ffd3b0ee2e8c1c8b218540a111a56932a3cdb4b2dca3805537d5a23`  
		Last Modified: Tue, 30 Dec 2025 01:54:27 GMT  
		Size: 3.2 MB (3170327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca4f8dd7e8bc459f3b31931b814f3dd67d3eba0ead6c52c08d03fe5885f6d4`  
		Last Modified: Tue, 30 Dec 2025 01:54:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83956e37af31ed691735a824abf11a19eb1e8ef47d3b3916bf546561e9d4459e`  
		Last Modified: Tue, 30 Dec 2025 02:00:16 GMT  
		Size: 33.1 MB (33099235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce817a6f503be53c3e17d4eeab19b64e281ed6c1057ae0919ee946de2bd7d4`  
		Last Modified: Tue, 30 Dec 2025 02:00:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b245df3fcb798fea81de895f23228278fe0b6cf405fe8c96b15ad8118632f2`  
		Last Modified: Tue, 06 Jan 2026 18:35:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a1337e2dc3cd3fc2549b686bb7b37a9f838465fa60e6a23f53eeb0e970302d`  
		Last Modified: Tue, 06 Jan 2026 18:35:14 GMT  
		Size: 118.6 MB (118620899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfb496f72e5a6644c8ece382bb065d266404e7dafe1fe03d2ce3d32fcf50b17`  
		Last Modified: Tue, 06 Jan 2026 18:35:08 GMT  
		Size: 919.3 KB (919258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce640d33d749a60092795a6e57c8cf0ffc284bef072e9e8a6e3186cfe4132cd6`  
		Last Modified: Tue, 06 Jan 2026 18:35:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f754a4060f8c8e154ae4c9b9fe53c13902f04d2e1104bd568a39867f0fd5d0ce`  
		Last Modified: Tue, 06 Jan 2026 18:35:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788d8be9652d4db580ff5f2c36013b870eed4193b8e2f64609f584ba2db3966e`  
		Last Modified: Tue, 06 Jan 2026 18:35:08 GMT  
		Size: 3.3 MB (3252919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fdeecde25be992ac09e707a617a4c8cb7b8130a045568edc3f68d0c3ed6b19`  
		Last Modified: Tue, 06 Jan 2026 18:35:14 GMT  
		Size: 65.3 MB (65340289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e37711db52b9f6dd9578519f9fad6656a8f8f05e107b4ece12873ff7f71695`  
		Last Modified: Tue, 06 Jan 2026 18:35:08 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:36864c8a1e3153678faabbeccf1017b9f7b3f9c4ad180c6b614da23128494d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd6071e8b7f36a25c2468a9a6e049f0bf6010c23b3f0b359fc2173be3845232`

```dockerfile
```

-	Layers:
	-	`sha256:21e7f3cd4894ff59c3e7568a870bb9f5f4a2b7ab25e2991705cf513f82bcec1a`  
		Last Modified: Tue, 06 Jan 2026 20:51:44 GMT  
		Size: 40.1 KB (40147 bytes)  
		MIME: application/vnd.in-toto+json
