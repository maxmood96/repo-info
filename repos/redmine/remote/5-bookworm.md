## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:52046a7d7db1a61abb6fbcb04bcfedfb0b10522b7c78ed54844bbe89db463e60
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
$ docker pull redmine@sha256:5b6512ce5f229bf3ed3f1ec5638d9f6e2c7400be5aed06ba4d7838ad051c519e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249314343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f67d050e5aeeadbdbeff0ce7785c82539b3b9ff81e6057f74c7a6d751f8fd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:54 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:13:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:13:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:13:38 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:13:38 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:13:38 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:13:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:13:38 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:13:38 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:13:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:13:38 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:13:40 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:14:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:14:16 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:14:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:14:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:16 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:14:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720da4786f774f8d50db8269e399bff3b9e1bbe5e88660c364c3726d3d0e661`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 3.5 MB (3510177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d642b6c07a15b274745714c90ba586bbda858c0743c424e25c4fe65f9e72638`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0de75d88464c3b86f05c31ec678872cfc37965c2310aaeb0341661c22d8b40`  
		Last Modified: Fri, 27 Mar 2026 18:33:04 GMT  
		Size: 35.8 MB (35781138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a46dbbfef6573a04e2100855782d74436470062933cd957ff448cd366aa16c`  
		Last Modified: Fri, 27 Mar 2026 18:33:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aa360df07b04345c48448f1cb424f3357fc0ba66a3fe857b9abcb8f182f10`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6359b2228f113bee6da9c4907cf944710663550f5d5cc48c53ea9271344d02ef`  
		Last Modified: Fri, 27 Mar 2026 19:14:36 GMT  
		Size: 123.0 MB (122952191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fcb9072b50c187a9ddbf3eb3d1751cc88794f2ce2a741bd69a614fc3eed4c4`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 947.2 KB (947218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a24791762162b4ecdfb5f5285abcadb708ed7ed6b68d3a113319b85dbe5817`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb205ffece44a5e025c5cde1c324b1ed1c02bfa43a3b43e8a54a286dc356305`  
		Last Modified: Fri, 27 Mar 2026 19:14:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e348783e7746e3c90d9f972a6f45ff35adff21864c7c18a88f66a029305608e1`  
		Last Modified: Fri, 27 Mar 2026 19:14:34 GMT  
		Size: 3.3 MB (3253541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37335de16aa17e842e903aff6d1314b11507821eadeaf8026400fb4d0b068acc`  
		Last Modified: Fri, 27 Mar 2026 19:14:35 GMT  
		Size: 54.6 MB (54629735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de9c26687b66459d077abc6f65b61c9404559c1d49214ecb8ce2ae8f4807f42`  
		Last Modified: Fri, 27 Mar 2026 19:14:35 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:ab16d10f1d7b530ed02217583afee62fa0829322dc322e57e886817a1c67d577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b902c29a18e7f58d7273c9033a86c8e379d549842164586fed84d5d6aa432`

```dockerfile
```

-	Layers:
	-	`sha256:cfdea0a879b184dee591b41459e6ce0c49085abfb5ddea99a170c25b764d79f0`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 40.2 KB (40159 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:51e8b217489e0dc6cd3c64addf370143638d7d655d8ce6186119dac5a23e3a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233534229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669ae473ca5c530f8f2d5b7b115d17783143147b653ea32c6c80ab2b24af3eec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:31:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:33:47 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:33:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:33:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:33:47 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:15:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:16:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:16:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:16:29 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:16:29 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:16:29 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:16:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:16:29 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:16:29 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:16:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:16:29 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:16:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:17:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:17:12 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:17:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:17:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:17:12 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:17:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0509921ab3afd77666b790895956e135e1e2fb4d8f883e8875dc39cf1523d`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 3.1 MB (3081057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acab53a82fd491be855c7b0fc4a36c627f104b6c3263bef951fe827b8d4ca6f`  
		Last Modified: Fri, 27 Mar 2026 18:33:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c621ddf033909815378f5cc2169fac84a35fbc3f726e689ee8350fe4223a284`  
		Last Modified: Fri, 27 Mar 2026 18:33:57 GMT  
		Size: 32.1 MB (32078792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5592a792a05e3913768ff79d875f8b92fc9d6e060001a5f4cfb79378dc86ae5`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52139f42e8a39b945e63985f62d90eb8330bb25cec1ec0c99987a0dc6dfb761`  
		Last Modified: Fri, 27 Mar 2026 19:17:28 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fc143594e2b6f3b20afbc06477c3dccf78b162d03af40f650f87973be1b553`  
		Last Modified: Fri, 27 Mar 2026 19:17:31 GMT  
		Size: 116.6 MB (116631751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de67fd7380a9392b5b5d0834a99180080b63878ff55bbed94e99b4081b4dfc2`  
		Last Modified: Fri, 27 Mar 2026 19:17:28 GMT  
		Size: 916.8 KB (916769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca959d9b3286dd8c69338c27bff79ea77045bd78db7aa665d4912b9d8c673e4`  
		Last Modified: Fri, 27 Mar 2026 19:17:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a009fb76222e2fb6ff334c4184242420601b0269d74bad4b3abcd84b1f92908`  
		Last Modified: Fri, 27 Mar 2026 19:17:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e436e94d1e1cd8fad24d9b868b4d7be03cdccf2757b0c3ccfc0ec4d9bc6f9a4`  
		Last Modified: Fri, 27 Mar 2026 19:17:29 GMT  
		Size: 3.3 MB (3253558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4967775f68009035448ed95d9085cb2f31e919294e1d8b75906590397003978`  
		Last Modified: Fri, 27 Mar 2026 19:17:33 GMT  
		Size: 51.8 MB (51802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a175aa78a6285f05a1a36c6ee5057fab228fda3f9c6923de67adbf49056cb`  
		Last Modified: Fri, 27 Mar 2026 19:17:30 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:fbd552a397c22ed993e82eaa186ba11cf3b08ca58897fcdee2cc2e8cd878c972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995266f5ad2ddd5918a75e89a517a8aae2a5151792149b404510bb58b09dc666`

```dockerfile
```

-	Layers:
	-	`sha256:03381d17e7b4f44d9a2f02b8d882d00c600ae02a24017401806e35ad416d6487`  
		Last Modified: Fri, 27 Mar 2026 19:17:28 GMT  
		Size: 40.3 KB (40296 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:080a73b06eb4266764baf7d879c069aeca9bc4d54ccf64fb22012f688d4e7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226594867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a579acd43caf3591ec92f7d02ffa4464ff119cf6e9213a14c4151c035e7623`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:11 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:11 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:11:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:12:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:12:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:12:01 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:12:01 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:12:01 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:12:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:12:01 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:12:01 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:12:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:12:01 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:12:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:12:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:12:40 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:12:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:12:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:12:40 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:12:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f749ab8f1791ed041d0530e13b98c95fcbbb10309364f9870dab9c3ebc63a0e3`  
		Last Modified: Fri, 27 Mar 2026 18:32:19 GMT  
		Size: 2.9 MB (2913749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b85973033435846f63211a0e6d84df6f59c91fee986c4cfe8e6afda18fb45`  
		Last Modified: Fri, 27 Mar 2026 18:32:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22859a0ef0349e1365deaef26124871c19d64ec4ab2a695b01ae8d4e82647e`  
		Last Modified: Fri, 27 Mar 2026 18:32:20 GMT  
		Size: 31.9 MB (31909950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080355c19138d7ca4214a6834881f793e5de716b880a70ba0ca8be3fa48358da`  
		Last Modified: Fri, 27 Mar 2026 18:32:19 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ecee1ca1cac965cd4714325934f5eadea91e17393fc642f72a885d50c67f0d`  
		Last Modified: Fri, 27 Mar 2026 19:12:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a07c8261bbb6f35d0db87ed5756607843d0837b0a80ebe6879f6144804ce8b`  
		Last Modified: Fri, 27 Mar 2026 19:12:57 GMT  
		Size: 112.0 MB (112025842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26a49505f12f2d9bcade32335434cb164b54085ea25318f289798d7c6a710d3`  
		Last Modified: Fri, 27 Mar 2026 19:12:55 GMT  
		Size: 912.4 KB (912402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c2b71eaff781e914b1555946b351154e3088c1c055f3278a680afa7df1c3f4`  
		Last Modified: Fri, 27 Mar 2026 19:12:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9290d94a5e0de9e6e3ebed599e85326755eabfec97fce6f591149153a4422c6`  
		Last Modified: Fri, 27 Mar 2026 19:12:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e0a81d8650fdba9b074e2cc6d6041e027f5faf35354cf86d18403fda2efabb`  
		Last Modified: Fri, 27 Mar 2026 19:12:56 GMT  
		Size: 3.3 MB (3253558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36744560f98ef1bfb0cc707c3d2665f042ae56457b0e0a4c631cecce9fa7dd1`  
		Last Modified: Fri, 27 Mar 2026 19:12:58 GMT  
		Size: 51.6 MB (51633902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734125de9d49c32c59592c8bce6e757b7b8f138a3e4a3ab25f60b59cb863a151`  
		Last Modified: Fri, 27 Mar 2026 19:12:57 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:08240923979f1afca9f4a4dcfb672bed3000c42167ee40871b257bdcf8251a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2d3a5944b7ba4e324f5542ea5748716b73b272b7f46705315125bf226eca34`

```dockerfile
```

-	Layers:
	-	`sha256:ea05991dc7df52418950004097046891a6f5485871072d7d0e34ea4ab3402750`  
		Last Modified: Fri, 27 Mar 2026 19:12:54 GMT  
		Size: 40.3 KB (40296 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:c272e240af4012f92597cdcc071dde6fcae9a257bca6f9578ac24b67b25abeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245739605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340b7aaed923b258afa08f82425382da60df9c0d2c3fa877d6e631f994fc5c46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:21 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:21 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:11:53 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:12:23 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:12:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:12:23 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:12:23 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:12:23 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:12:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:12:23 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:12:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:12:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:12:23 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:12:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:12:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:12:58 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:12:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:12:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:12:58 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:12:58 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2bf29c161d4b803874a4a08b0e4cc7ddfbeb28ff4cb0f9250fa2091aec487`  
		Last Modified: Fri, 27 Mar 2026 18:32:30 GMT  
		Size: 3.3 MB (3341466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f3635f949b1ab6e024c4f0132bebcc74ef2c37d7f9f15fa2104d9c02701c8f`  
		Last Modified: Fri, 27 Mar 2026 18:32:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e98fb07534e2ab6d3659470de49ced2eb1db0d89cf522434f91e39a71e75295`  
		Last Modified: Fri, 27 Mar 2026 18:32:32 GMT  
		Size: 35.7 MB (35687892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228cb8d5c23dc24db4673bb1850afd347fb1f213ba80fbb685958d8c3c7c891`  
		Last Modified: Fri, 27 Mar 2026 18:32:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c5bb21b8b590b408eebed46d764eee639fa566c647413cd2a7192564f35aba`  
		Last Modified: Fri, 27 Mar 2026 19:13:14 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab7dcf2c7e84180cf3713f55dc00d412bf12fdeaf6fda4d6d5d7dfe4c381d1`  
		Last Modified: Fri, 27 Mar 2026 19:13:17 GMT  
		Size: 120.4 MB (120413801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97ce2aa183a97d88d257404fa02c03992d829b7277d6759c4dec4e3633b313`  
		Last Modified: Fri, 27 Mar 2026 19:13:14 GMT  
		Size: 900.8 KB (900759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d817ca8010cd011355a4a2805f3dd9a7c2f11e0df180ebfc4c6686f6bfc53b`  
		Last Modified: Fri, 27 Mar 2026 19:13:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80832442b9219a7f66375e3b7802d377e8694c29b3cdd2c2c7cb6e394c2d39fe`  
		Last Modified: Fri, 27 Mar 2026 19:13:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82d830a6e87a2d82dfbcf2e6efa0f19206192adbeae75ef381d3cf8f32658a9`  
		Last Modified: Fri, 27 Mar 2026 19:13:15 GMT  
		Size: 3.3 MB (3253564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e34d10293043bbb91b6c071125472cc96a5fe92de5d16066321d2d23c93228`  
		Last Modified: Fri, 27 Mar 2026 19:13:17 GMT  
		Size: 54.0 MB (54021942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5078bc8a3953b71800edc06e1da8dd192cece82de8531bf39d7f11e76ed43a6`  
		Last Modified: Fri, 27 Mar 2026 19:13:16 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:cb4258c3db04c5151fdbbbfc8cd150587745891ea1b5d94cdccdfe9e4f1d694e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75938a4c93251a821570e84583e46589e7ecb994011426883c7ce52ab8b8b100`

```dockerfile
```

-	Layers:
	-	`sha256:f0798911a7b190df673a629f99a3432b6f13fac2bc7a13261c31b8b4d09e8b42`  
		Last Modified: Fri, 27 Mar 2026 19:13:14 GMT  
		Size: 40.3 KB (40326 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:ec03340def8a9f11d3d73ce81b670570427c534d561720540d606fcc4bbba156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247518404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5be5c5e3c8655603c8a76e5117d7ad926198be9ac63cf2bc4c8f0467d4b574b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Fri, 27 Mar 2026 18:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:30:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:33 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:33 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:12:20 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:12:53 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:12:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:12:53 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:12:53 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:12:53 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:12:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:12:53 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:12:53 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:12:53 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:12:53 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:12:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:13:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:13:34 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:13:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:13:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:13:34 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:13:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be82ffbcf8ae3cdc7b1e40d90551ea955c0ea03e9e844610ffc274b66f9e82`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 3.5 MB (3512915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef216bd1074e05ab1fb22dff507b71b91d11763ca49bd7be4c5958e1d0f753c`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9630165582738c6fc95fba61bcebb6724044d6f804aa3010c1c1fef82f9147`  
		Last Modified: Fri, 27 Mar 2026 18:32:42 GMT  
		Size: 31.9 MB (31884076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12128aab6ee45e8777710bbe7a6f5f738c643fadacf4178a7d4445a4891aa9e3`  
		Last Modified: Fri, 27 Mar 2026 18:32:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d201da9fd6d59d245339e304a70990b88661b6615d6416b13c3938f5dae15028`  
		Last Modified: Fri, 27 Mar 2026 19:13:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d7b6cfc045b9ce1a38d76613f8a6c170c1f3fa026caf57097ab61a5775ba5`  
		Last Modified: Fri, 27 Mar 2026 19:13:53 GMT  
		Size: 124.8 MB (124832882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e2441100dafe40cc68377fd6013576b0b8c5cc9b4874b32a696d7f7e676f92`  
		Last Modified: Fri, 27 Mar 2026 19:13:50 GMT  
		Size: 915.7 KB (915729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c889b566c1315f012da1c80304c62a42f19a3754557cbf54ee9da05ff41f37de`  
		Last Modified: Fri, 27 Mar 2026 19:13:50 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b5b08c3ae6acb63916253ac300c712f3d470a9624ed276676ad4d7fb7ede3`  
		Last Modified: Fri, 27 Mar 2026 19:13:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd81998dd694c25e1c1817b3bec10469c89fc03860fbc8d252527e68ce472e1`  
		Last Modified: Fri, 27 Mar 2026 19:13:51 GMT  
		Size: 3.3 MB (3253564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33906b54d09ba3f9633eb1d6274c490c3ab92ca9bee1be90c46062d73019a02e`  
		Last Modified: Fri, 27 Mar 2026 19:13:53 GMT  
		Size: 53.9 MB (53893440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15306ec98b0f2b0373520a053530f3f6ad9b59a3d3fb499007c56cff265d7c5`  
		Last Modified: Fri, 27 Mar 2026 19:13:52 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:c845e1fb9503a5a4166f39bd3490b9d8f3d147bec1e3c726bdcf8b919061caaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b827bcf7676162cbffde79d54215978dcbba0891dec4725541aca92e6cc32c1`

```dockerfile
```

-	Layers:
	-	`sha256:2155d63c7243f1ae7d5042cecde372207b4eee714d0e6a056a9ba4de34e33533`  
		Last Modified: Fri, 27 Mar 2026 19:13:49 GMT  
		Size: 40.1 KB (40122 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:e951d1b1d5f641046043ef24891e95ada88c3286bf41030edb4bfc5b661e730d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253163933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a4eaf7d60594129e3057ec9109836acde350a1861d98b4a2bba1a7bfd70c75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 13:49:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 13:49:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:54:31 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:54:31 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:54:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:54:31 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:54:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:54:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:54:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:54:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:54:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:54:33 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 20:13:50 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 20:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 20:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 20:17:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 20:17:38 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 20:17:39 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 20:17:39 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 20:17:40 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 20:17:40 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 20:17:40 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 20:17:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 20:17:40 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 20:17:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 20:28:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 20:28:18 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 20:28:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 20:28:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 20:28:20 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 20:28:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:036b690c37cf2dc49974818e200658ce29b93c4d917171332d28ada375e6f68b`  
		Last Modified: Mon, 16 Mar 2026 21:51:40 GMT  
		Size: 28.5 MB (28526147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5901c5b4b386661d4ce2f3c81157de4436091432a87e38987901d3ff0e6b4666`  
		Last Modified: Tue, 17 Mar 2026 14:21:15 GMT  
		Size: 2.9 MB (2901270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e17e07076a73b2c5b3a253b5365c50280aa824aef788c8c57ca584268f3e8`  
		Last Modified: Tue, 17 Mar 2026 14:21:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce269f098f7cbc734809e992b1848564e979a5207a3e0bc5a34526a629d2c70`  
		Last Modified: Fri, 27 Mar 2026 18:55:10 GMT  
		Size: 33.1 MB (33127381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb941a5dd81b9f8484cc6fa7ed4e4b81a67cfe05ed57d277733aee3bb27b3`  
		Last Modified: Fri, 27 Mar 2026 18:55:06 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50710aaeae0ef41fe4d169823a0b8ae0027093938018a4683786a72af7a3ba3`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f750eb136835a880b51e31c7532eb83609010b3180ba5bd7b0599e1d625287`  
		Last Modified: Fri, 27 Mar 2026 20:30:51 GMT  
		Size: 118.5 MB (118453006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10634d08de44db1e05fce5bc063a9846ac0b8267be1e9506a2f6e8a7838bcfeb`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 857.3 KB (857326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ba7616c443abc5ff5e8fda6efb49d5002707d56a5b0e2cc108ebfe012469ef`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342fa6d1c27555473862707c471d42151081b440ee1de8c03634a9dbdabd3423`  
		Last Modified: Fri, 27 Mar 2026 20:30:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0969c643b73ec185825bf379eaaf1b98621b958ebbbddebef7fa9252dd575f25`  
		Last Modified: Fri, 27 Mar 2026 20:30:35 GMT  
		Size: 3.3 MB (3253554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc30559a38a44ecefab8643237b22fecb249353fe7adb7e14b76e7adfa9080b`  
		Last Modified: Fri, 27 Mar 2026 20:30:48 GMT  
		Size: 66.0 MB (66041131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a085a6225f3a21528f31a5279e6c2e2956e9e231beee4947c9cd06b34b0f74ff`  
		Last Modified: Fri, 27 Mar 2026 20:30:35 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:be85e739f1ea60edb6ee0435f1e47d6fa60b023e7c2d3272068563705078e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d747448d2b711caeb0113ba943dda34e0d1a52b64684385a7e6c8ce46f2b7bb7`

```dockerfile
```

-	Layers:
	-	`sha256:b405b5939c29ea274d74336b4b92ef25c8e62dec888290c653945aa8095de66b`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 40.2 KB (40231 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:d17c66a9a3fda620cfee75953247c62947e79063946e1de1819d09d29f5a119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270378325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacfd199246da4d45e5b92533032b03590ab509bb185187e1092e492ef09d73f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:37:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:37:55 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:39:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:40:50 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:40:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:40:50 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:40:51 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:40:51 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:40:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:40:52 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:40:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:40:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:40:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:40:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:44:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:44:32 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:44:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:44:33 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:44:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6dd432af990aeed0dd4fd76d6d1fe507bfd33f78826731a1300e5c6f93423f`  
		Last Modified: Thu, 26 Mar 2026 18:35:43 GMT  
		Size: 3.7 MB (3710764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73847511305cedc00f17cc76877ca78c47c8d883a71664a7a3430ea3065709fa`  
		Last Modified: Thu, 26 Mar 2026 18:35:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec79745a4682555cfd3bbd00deced64e2558785bed015802f59239a475cc4c3`  
		Last Modified: Fri, 27 Mar 2026 18:38:14 GMT  
		Size: 33.6 MB (33627300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf3905224c31d262cdb12adc36066b5968e6248de1c9d70415996c492692f0`  
		Last Modified: Fri, 27 Mar 2026 18:38:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536374234d930a73eca536f7194b62f1899a96c3d57fb9bece0e191e635cfa57`  
		Last Modified: Fri, 27 Mar 2026 19:45:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8b73f7e119c7480d302e9f8af0c6f70bb4b2be6dff87aae64929d285d23c1e`  
		Last Modified: Fri, 27 Mar 2026 19:45:13 GMT  
		Size: 129.9 MB (129931076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46042c669a051a382bb83656455fe153ae86ffef1ac0c07d6f1f076361ee0a`  
		Last Modified: Fri, 27 Mar 2026 19:45:09 GMT  
		Size: 906.6 KB (906573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aa3b68250673c4f39e4e36eb3357f7bfddc07d9ef98a47e9f864268798a867`  
		Last Modified: Fri, 27 Mar 2026 19:45:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9640d01e9408d06f3456b7230e5d965844a59c10c4d37c17e2cbf2ada5b51255`  
		Last Modified: Fri, 27 Mar 2026 19:45:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee04f1d1d0ed991eede72a70db8edc54a72b573855ac7a4573ea5fad508b37c`  
		Last Modified: Fri, 27 Mar 2026 19:45:10 GMT  
		Size: 3.3 MB (3253562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc35c376155e887ebdf02ffa181e61c54b8b8027e2caa2b82c4195ecff9979db`  
		Last Modified: Fri, 27 Mar 2026 19:45:13 GMT  
		Size: 66.9 MB (66866568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a43cc73757bb3efad015777b368c660284babe49db59a1158709f0a7e8a5ac9`  
		Last Modified: Fri, 27 Mar 2026 19:45:11 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:35997d6b7407e1b773cf3e17a7aa43ad9fd4b32af70c7845fae6d8f677b2a781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369b8606aeb76017588b872c47570dec2060c026f9b03b0de194360112d200c`

```dockerfile
```

-	Layers:
	-	`sha256:829f0fdbb351036aa9684e8e043df79ee69b01e98203d2e143ff8cce30a25322`  
		Last Modified: Fri, 27 Mar 2026 19:45:08 GMT  
		Size: 40.2 KB (40205 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:ed51d8c6a28998d06b5cee765b7947ecc5797a5098ff3d9e6fb690ca692d3de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250659661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b644249187f5bbbb2c087d6ccceb3b14117fe220ef45e3af6c5e4a137142d743`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 18:28:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:31:12 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:31:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:31:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:31:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:31:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:31:12 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:11:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:12:10 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:12:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:12:10 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:12:10 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:12:10 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:12:10 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:12:10 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:12:10 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:12:10 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:12:10 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:12:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:14:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:14:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:14:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:14:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:14:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa423bc82dbe9900983364c79e98ab227be4db425af41a7c5ddf086cb1442cba`  
		Last Modified: Thu, 26 Mar 2026 18:29:16 GMT  
		Size: 3.2 MB (3171221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04c640b78ba55a660ffb68f109902ea1388e342f84298445d0a8e9b778ab6ec`  
		Last Modified: Fri, 27 Mar 2026 18:31:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d06d395c0114f0c458dbb46affdaca647bac522090cf8b13de69cd9e6c6bda`  
		Last Modified: Fri, 27 Mar 2026 18:31:28 GMT  
		Size: 32.9 MB (32875224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ca8834f25ee1e990c6f4f11d81385b6db6388d3c3777a86d6e447acee6a75`  
		Last Modified: Fri, 27 Mar 2026 18:31:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be34d810bf185ec37ebb5bcd30f929e40e3692ca1a8812e67bb442b4f0af73da`  
		Last Modified: Fri, 27 Mar 2026 19:14:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6290e86d316322487d052434ec3212fbead64b6e3b9a393df8a83bf8c94b3`  
		Last Modified: Fri, 27 Mar 2026 19:14:33 GMT  
		Size: 118.6 MB (118628140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3f863f3be8871afb7dfe4ec75c3f1fea5e2422879f25317dcb08859628144a`  
		Last Modified: Fri, 27 Mar 2026 19:14:31 GMT  
		Size: 919.3 KB (919251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666d42e8f9e0393b101eedf5e1af9fe47091d604ffb1afbddddb78326f5cf9e`  
		Last Modified: Fri, 27 Mar 2026 19:14:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb5571ce00452fbe2a8ce4b24bb42872c0895b789ff68121f0eed431325ff05`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aa4915f52badd81a6460641bb38e137a14aa1e489ebb0cf69220374e99a130`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 3.3 MB (3253558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1e15cbb8c05586022378d266238ae83e2a81b23f37e601e9bda66d4e864714`  
		Last Modified: Fri, 27 Mar 2026 19:14:34 GMT  
		Size: 64.9 MB (64916634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1e017c21da7b39f82773218831574191966dd7a2e8489c69502388cae0bcf7`  
		Last Modified: Fri, 27 Mar 2026 19:14:33 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:1484ad16642bb946a4577ab68b6a61706d1b4598cd62d7a271d3efacb1146d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da02d450497932dc5be14f7daa026fec7dc24ab500742373b89ffbbffcb30f85`

```dockerfile
```

-	Layers:
	-	`sha256:88439b2dddd0b952548148bc41ef245f597ffb084cac474c9c6b30542764ccf9`  
		Last Modified: Fri, 27 Mar 2026 19:14:31 GMT  
		Size: 40.2 KB (40159 bytes)  
		MIME: application/vnd.in-toto+json
