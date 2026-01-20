## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:f5ba09196fc3d370cb47e2c45f945fc8a7d97ec6885706425ff44d42d72e9e77
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
$ docker pull redmine@sha256:0495703ab4114ba4337339a84e85bc6e162f6a871c12badfe819469257fbda42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249518137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202be5de1f6ce830996cae34d35f2fe2792870308dae36262d06d476add4eff3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:00:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 18:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 18:00:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:00:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:00:49 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 18:00:49 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 18:00:49 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 18:00:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 18:00:49 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 18:00:49 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 18:00:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 18:00:49 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 18:00:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 18:01:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 18:01:25 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 18:01:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:01:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:01:25 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 18:01:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992d85d4bb153b953b57ccc4ad423d042837aeba10255d229ae9a12a47bdea6`  
		Last Modified: Wed, 14 Jan 2026 17:36:04 GMT  
		Size: 3.5 MB (3509960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f8207ae9bcf98be8497b1a7fa74edb6df1804b698df6cebf00a2256c10d06d`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc2145f95b9316ebbbf5428843e5d4a983e07877d6697399deea1ca33e04fca`  
		Last Modified: Wed, 14 Jan 2026 17:35:55 GMT  
		Size: 36.0 MB (36010912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11116098be267a65bdfbb06c327810aed28e5711f8ef8176502171556752a64`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d8b34baf0b876ccb876853673152a2fc268bbc4c90863b59cdbc58801b57e0`  
		Last Modified: Wed, 14 Jan 2026 18:01:51 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69c988a6cae3095effd2fc6a1451506ebd336b65ef8c36ad651376f7d2af9b`  
		Last Modified: Wed, 14 Jan 2026 18:02:07 GMT  
		Size: 122.9 MB (122946378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71112c42c90861643fe7a94191ec902d8437c7cbb009c8e89b9645a7d19c79`  
		Last Modified: Wed, 14 Jan 2026 18:01:52 GMT  
		Size: 947.2 KB (947172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f663019742a2ea0d1f4afe9e87476096a769375fec66a68358ec279ee6ad4`  
		Last Modified: Wed, 14 Jan 2026 18:01:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de76b1bb790e16fc07d18b835c41fe435aab721ab8392fe83295540d4539b8`  
		Last Modified: Wed, 14 Jan 2026 18:01:42 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ab75c63101f5d6702db69bf60c8ff055530f74c28981495e8513f275468536`  
		Last Modified: Wed, 14 Jan 2026 18:01:52 GMT  
		Size: 3.3 MB (3252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabdc2d9cc77bf2ca3ba9091e1a6af5e384fdbf881a3f126feea96e98bf8116`  
		Last Modified: Wed, 14 Jan 2026 18:02:00 GMT  
		Size: 54.6 MB (54618099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef11fef21905074c92037610fe0aa680cbdc954a36872359f162b1503a48975e`  
		Last Modified: Wed, 14 Jan 2026 18:01:44 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:5ce27736888dc5aebe76f58e49ad96c9c49cb3b976cf0ad8753801338b1a39b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05830941ace1b9080a6159dd5a94791118c5da14311be070f4e2fc411f071066`

```dockerfile
```

-	Layers:
	-	`sha256:abff20970ce16cc3bf733f4469bf34af5641a0627f303d858f4d0ca3c3e77206`  
		Last Modified: Wed, 14 Jan 2026 20:51:22 GMT  
		Size: 40.2 KB (40159 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:f90b55fde88a5b27215d2b5c9b9eea78e5e2cb4a26f83fb169d6a34591dbceb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233753416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef56c705a3cc9401aa8426f9047f6130bdf9222f5b5322df1f7bdd87f8612606`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:35:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:35:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:37:42 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:37:42 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:37:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:37:42 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:37:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:37:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:37:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:37:42 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:37:42 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 17:56:15 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 17:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:56:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 17:56:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 17:56:59 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 17:56:59 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 17:56:59 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 17:57:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 17:57:00 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 17:57:00 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 17:57:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 17:57:00 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 17:57:02 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 17:57:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 17:57:48 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 17:57:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:57:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:57:48 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 17:57:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:43595593b17008d0147d9ea53c9ed04f4ec8fde216c1d359e2de9daa9e0665f6`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 25.8 MB (25757697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d2f60ae02684aab841720de6a7d4d72d21ddf771bd0bc27845c2b9406606b`  
		Last Modified: Wed, 14 Jan 2026 17:37:58 GMT  
		Size: 3.1 MB (3080659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fcc0815e187f05649b048a99082481233ad10f875fb908a4f689a833ab7ec9`  
		Last Modified: Wed, 14 Jan 2026 17:37:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7ca4757baf38a117c421a10787f683508aaba5657a558498c074e2d78f597c`  
		Last Modified: Wed, 14 Jan 2026 17:38:03 GMT  
		Size: 32.3 MB (32331057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9dc4669b6c4333bfe78877cb21d40b3be1046fe124f3dae8d67ad56926ac58`  
		Last Modified: Wed, 14 Jan 2026 17:38:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb314acfdb2b2d8d6a4ed7f7f1fa4b2ee62dd24d4c168e0208c8ebe024c50f`  
		Last Modified: Wed, 14 Jan 2026 18:21:03 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef6a85f190bf45da5260fc073ad6373d21388405c1a32da833ef8b8c69f8ecb`  
		Last Modified: Wed, 14 Jan 2026 17:58:28 GMT  
		Size: 116.6 MB (116613393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f7ee42b64b9347333ca8ca62b3e2549dd8554efd26c4acbaccf7225ee23a19`  
		Last Modified: Wed, 14 Jan 2026 17:58:13 GMT  
		Size: 916.8 KB (916765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a54cdcbdd87908d4f61f852d68d3125c9df0e4351e57987411f4099359c1d1`  
		Last Modified: Wed, 14 Jan 2026 17:58:04 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68470aacdae266e36d69c7597436a1d10de3f68d56843dbc26473d9837b6f065`  
		Last Modified: Wed, 14 Jan 2026 17:58:13 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8c6753c271766e479a6588df727a37a84f8f83318066e8499dd9dfe472cdf6`  
		Last Modified: Wed, 14 Jan 2026 17:58:18 GMT  
		Size: 3.3 MB (3252934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b08a5ae1ad97236a92cbc348cd9f4747621288afeb48e995868362a2cff0656`  
		Last Modified: Wed, 14 Jan 2026 17:58:20 GMT  
		Size: 51.8 MB (51796793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d500e248d8b1a397367aed0c239dc0877869b77c5830d316154c69aa93eb831b`  
		Last Modified: Wed, 14 Jan 2026 17:58:06 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:6fea7514ed92a76f431aa685246e953ebe581269fd7960e0918951fbecb18ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714295e09095c51f1a0166ca9753d8698ac64a6871544de1a14d280ab74e0cfb`

```dockerfile
```

-	Layers:
	-	`sha256:046d6c0db9a3a1286f31f1e6f421d4f4e247294f4191c6f33e61b1fa0f6f0609`  
		Last Modified: Wed, 14 Jan 2026 17:58:04 GMT  
		Size: 40.3 KB (40294 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:b1c032b899952871834a7a6f78d69e4611aae8a801510edd94843289e24d53b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226830471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1437afdab6607e42f59102f9b1fa0c48672fbfe778b2ea9420a8590f5701a4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:06:18 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 18:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 18:06:51 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:06:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:06:51 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 18:06:51 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 18:06:51 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 18:06:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 18:06:51 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 18:06:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 18:06:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 18:06:51 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 18:06:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 18:07:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 18:07:29 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 18:07:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:07:29 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 18:07:29 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bf99e624f48fb7f11d92926014124333deec81b36a9ccd999d1842139fe22d`  
		Last Modified: Wed, 14 Jan 2026 17:36:01 GMT  
		Size: 2.9 MB (2913517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1544acf04562f4514e672d1a2f75a870b2aafb8b1a0cd3e74f8c5263cc6ab8`  
		Last Modified: Wed, 14 Jan 2026 17:36:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c33c777e42fded3b5f5b2856e6afef883f77414170170016846e32d70b673`  
		Last Modified: Wed, 14 Jan 2026 17:36:14 GMT  
		Size: 32.2 MB (32167678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85378b7a191212c5b5565e5c7d410bc801af4c95d436fd0ce2869c525c0dd8`  
		Last Modified: Wed, 14 Jan 2026 17:36:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b92e7ae1725ab6137779a08188277c2cfaffec1c6637792a2fc944ad101acf9`  
		Last Modified: Wed, 14 Jan 2026 18:07:44 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b064da7c259b15a44e049e32f3b9c4e3363aa1bfbaa2607a3e88379d5cbe110`  
		Last Modified: Wed, 14 Jan 2026 18:09:16 GMT  
		Size: 112.0 MB (112008437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f386a9396e9d35a75da33141daf029e1418cb3846b13cf5b90cb26e8f668b377`  
		Last Modified: Wed, 14 Jan 2026 18:09:02 GMT  
		Size: 912.4 KB (912358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3897354f420f85b0081c6e9fd570d8296d8d4c6a341c713215de2bce54c2ce17`  
		Last Modified: Wed, 14 Jan 2026 18:09:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959e07fd00d0396681bc497d5f7d8cb5ad59e80de8249a8cd97c6bdfca2feba9`  
		Last Modified: Wed, 14 Jan 2026 18:09:02 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf8f5b2673f63b6338a5c98f606e07acc043642e61c3ff97757a8e3cc813bb2`  
		Last Modified: Wed, 14 Jan 2026 18:08:01 GMT  
		Size: 3.3 MB (3252925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bbbe56d4af8742dfdf0b9681ae1a08b4f04f5756c37fc5ae689430afbabf97`  
		Last Modified: Wed, 14 Jan 2026 18:08:54 GMT  
		Size: 51.6 MB (51637325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14f2271b4cb97cf07588fcfa69cc78cea5c53dd3fc96bed768ea00bb2e0ce3a`  
		Last Modified: Wed, 14 Jan 2026 18:09:02 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:37108808ef87c53769f49d53759142e1543fa025f882f5ec03992832efedeaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04d3a482ed3b0cff458cd52d0988f69e91c30a564a352c58366ed3515c17631`

```dockerfile
```

-	Layers:
	-	`sha256:17526a5de6359f57301e016df3483e3ee23627159fed11ec8d2e1f4a3de0b470`  
		Last Modified: Wed, 14 Jan 2026 18:07:44 GMT  
		Size: 40.3 KB (40296 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:4be70a60a8bac453032da36e5711a05674dc870780bdf210ac18ec92cbba75ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245937224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d217989c9366f88c25c13ff02197336832bb75e760470d2c9a00f3e932841f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:26 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:26 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:26 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:10:25 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 18:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 18:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:10:55 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 18:10:55 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 18:10:55 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 18:10:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 18:10:55 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 18:10:55 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 18:10:55 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 18:10:55 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 18:10:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 18:11:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 18:11:29 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 18:11:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:11:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:11:29 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 18:11:29 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716ffb03dfc83b802f236f0682d9491d05f09b2aa0ba34ca262271c7418d7224`  
		Last Modified: Wed, 14 Jan 2026 17:35:42 GMT  
		Size: 3.3 MB (3341744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c48551022673b2b908ad5ef74ab8cc340004700e8b17c68a53ffd329211ca6`  
		Last Modified: Wed, 14 Jan 2026 17:35:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e86e816e37a1709db7a414e4ff0a4020f308faaa3b7422a2171ee625989d49d`  
		Last Modified: Wed, 14 Jan 2026 17:35:37 GMT  
		Size: 35.9 MB (35911923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d024c3e3223a9db829b2e5e509604636b2a322af5ba45ee436f1e00cddb7b2e`  
		Last Modified: Wed, 14 Jan 2026 17:35:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d3e0231d723f807a908006735efdc6bf8c6f0190d6382cb144a133b75a19c`  
		Last Modified: Wed, 14 Jan 2026 18:11:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eccc00ede3f181c84f0c8cfb0411a7684482e4c99cdcf56a67d94c5c7d979f`  
		Last Modified: Wed, 14 Jan 2026 18:11:49 GMT  
		Size: 120.4 MB (120417215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953bcdf7b11b38fe3a1038b71829f4eb95d9667b900d4d4a43b4a2802d783fa7`  
		Last Modified: Wed, 14 Jan 2026 18:11:57 GMT  
		Size: 900.7 KB (900742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60f1f4c8603ede6c7ce3a6151a15541477f0aeedc508faac611c08c35e3a098`  
		Last Modified: Wed, 14 Jan 2026 18:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0a30d8f3d3239af404ace586c181d39bb05b5156c8f493216375f99ace6d29`  
		Last Modified: Wed, 14 Jan 2026 18:11:47 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cc07a9548176a852ce204c215b9f6f2fa301d20f45205afeaf23b1acd4065`  
		Last Modified: Wed, 14 Jan 2026 18:11:47 GMT  
		Size: 3.3 MB (3252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7923093b170d605c79b31806e40d9f5220152dec927cff98a039541205bd7c60`  
		Last Modified: Wed, 14 Jan 2026 18:12:02 GMT  
		Size: 54.0 MB (54000663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795e8b9b109600b13edea9801bc81d285d95fccdb0572e7c0289fc637b6d79f`  
		Last Modified: Wed, 14 Jan 2026 18:11:48 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:4f8b7838645d32d5621fad234cc6cfa6f89cc698fb836c3487d3f8f7ddefa114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5974d56a13cac7c4a470d76d00a8c8f713f42af5c44b9b6cee9f0d0a8544a61c`

```dockerfile
```

-	Layers:
	-	`sha256:941359399e3753544dfae3a5c5c8b6d402cc1f5f5f10235407b2c5ca6057967f`  
		Last Modified: Wed, 14 Jan 2026 20:51:32 GMT  
		Size: 40.3 KB (40326 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:42bf90db7b02c1dbe2f6656ce4334c69fd60f1940125bb80f08c3b202f140882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247789856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735b85abfd757cc58559000614ff3aef0f95d4acab15a309782407552b931186`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:32:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:34:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:34:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:34:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:34:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 17:55:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 17:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:55:50 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 17:55:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 17:55:50 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 17:55:50 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 17:55:50 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 17:55:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 17:55:50 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 17:55:50 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 17:55:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 17:55:50 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 17:55:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 17:56:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 17:56:33 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 17:56:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 17:56:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:56:33 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 17:56:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664d00f2ac07f1a53ca39e59420e0ad3b6d744a8e067b9b3a188609503eb53f`  
		Last Modified: Wed, 14 Jan 2026 17:35:02 GMT  
		Size: 3.5 MB (3512267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d1341420adb4e4c0776dbc2c45d78e4e46e5bbd4f04b0c31a49bbe15301989`  
		Last Modified: Wed, 14 Jan 2026 17:34:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2403fe3099c18d48da4cc7428c35b8a06c8863adb203a578ac9e16bcbdb405`  
		Last Modified: Wed, 14 Jan 2026 17:34:56 GMT  
		Size: 32.2 MB (32162614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4bf5f4010fca07e2de4b4dd7164f04c8ed771d92761739e7d43985c46b87c`  
		Last Modified: Wed, 14 Jan 2026 17:34:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812882820bb92ad3b4b5773846e198791a8fd5a03c25b9722f2d84a8d8a6dd82`  
		Last Modified: Wed, 14 Jan 2026 17:57:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba7d00efbfa87a8a1307bff6ab730c360af57434c74e45a157653ab21a0f8f9`  
		Last Modified: Wed, 14 Jan 2026 17:56:52 GMT  
		Size: 124.8 MB (124812893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b48a80fdbf3367f09185873149355a51d058385f82352f2690f96a1e54525`  
		Last Modified: Wed, 14 Jan 2026 17:57:01 GMT  
		Size: 915.7 KB (915680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c35e5aa71e942c734d9be11962e38bf0e967e7a444868a3759146dab5d0a8`  
		Last Modified: Wed, 14 Jan 2026 17:57:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a08134e30fcb315450e9d49c2512a9468c47badc4e6754723a7909d403f9176`  
		Last Modified: Wed, 14 Jan 2026 17:57:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3914eadecc0f30631621799c3b101ef0a401f552ed6d93327d2dafabe86d991e`  
		Last Modified: Wed, 14 Jan 2026 17:57:12 GMT  
		Size: 3.3 MB (3252927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002285cd4a71d06945a9deef541eb7c17f983148a248e22fb4dbc0f13cebe2f`  
		Last Modified: Wed, 14 Jan 2026 17:57:06 GMT  
		Size: 53.9 MB (53919292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c857f5e26daf248ce1f52b953a4ee22ba5ee6386af64a900cd31d66090fec29`  
		Last Modified: Wed, 14 Jan 2026 17:57:01 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:dec7b0b19890f38fface2445cff873ee3ec7fa8fde3bb081e24d9734cfe95546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4c2222553eeeb44a16485b10d800cef86adc4ae0c838790261741ec13a5933`

```dockerfile
```

-	Layers:
	-	`sha256:c9ded740aa450e5d28e4753c8697c11bd9baa806dbf1681325f5bce39e6ee034`  
		Last Modified: Wed, 14 Jan 2026 20:51:35 GMT  
		Size: 40.1 KB (40122 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:9c8e2bd591c4444e8edc110a3e6c4402961dc3968c40213ad2dc32dae2351038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253409809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db8f1ecd1313b88d9201977d5eabb1e32c10566273b9a0a973a3385b49ad6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 20:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 20:33:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:57:29 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:57:29 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:57:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:57:29 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:57:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:57:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:57:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:57:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:57:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:57:31 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:10:17 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 18:13:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 18:13:51 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:13:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:13:51 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 18:13:52 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 18:13:52 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 18:13:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 18:13:53 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 18:13:53 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 18:13:53 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 18:13:53 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 18:13:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 18:23:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 18:23:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 18:23:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:23:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:53 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 18:23:53 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c063a3c188d3088513ac303ee5a03a6c0ddff0d68a1e46804a822134a25bf8e8`  
		Last Modified: Tue, 13 Jan 2026 00:40:54 GMT  
		Size: 28.5 MB (28513755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1475973bfe710f8bf8e4d6961949fe96725eae466338b8a078240a6c90c114`  
		Last Modified: Tue, 13 Jan 2026 20:49:31 GMT  
		Size: 2.9 MB (2901311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734cc8619a1728020176b76d211926967fa17bbc3afaea2b1294eeec3f994d16`  
		Last Modified: Tue, 13 Jan 2026 20:49:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ac43eb1b8d918eb3af52e846d2baab8c6dd1fe7593ba81258b948c4c161e96`  
		Last Modified: Wed, 14 Jan 2026 17:58:07 GMT  
		Size: 33.4 MB (33354494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdb0eb737ac6ed444d715f5b984d5e0c196529f76c52b9e30643896f8d6176d`  
		Last Modified: Wed, 14 Jan 2026 17:58:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e826f8a38e1d4ae94fb1f8b3a57102e980cf4d47fc52567116dc1a9add775ba`  
		Last Modified: Wed, 14 Jan 2026 18:26:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f3c9cecc20ca0521b0c7c053ebec6863389f533c941db2e6aec5dd82900554`  
		Last Modified: Wed, 14 Jan 2026 18:26:20 GMT  
		Size: 118.5 MB (118453523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c24bf29e8b34ddb1b3c6a0c7f719947cf2d6496d50695665d9992a2129821d0`  
		Last Modified: Wed, 14 Jan 2026 18:26:31 GMT  
		Size: 857.3 KB (857279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63799585c6c7578ccf36f24222619fd2864d155aa3f111968c9ef461ad059a36`  
		Last Modified: Wed, 14 Jan 2026 18:26:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a494765a74cf07ab617382ff4288479cfde208e3145c776180129e4bfae5d473`  
		Last Modified: Wed, 14 Jan 2026 18:26:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89878713b416b225886cf925d5d6eef8f9caeb852ea50273bf7ffca24af19c47`  
		Last Modified: Wed, 14 Jan 2026 18:26:04 GMT  
		Size: 3.3 MB (3252920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afea68605263eaaafc7dc015abd6f77411a5d368a6096a33aecaf5a19428601e`  
		Last Modified: Wed, 14 Jan 2026 18:26:17 GMT  
		Size: 66.1 MB (66072414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db66ecb71fb9e337deeab8815cd209665b2d0bbfbbe51428bb9f0fa86ae2ad`  
		Last Modified: Wed, 14 Jan 2026 18:26:05 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:82be2478ce81646fa0ac3f3478cece4a945a6095ff309b9a23e14f116b39a150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2872b8643fcd3681f7f10bdf88c640e7c72ec42c905e6d8cda8dd302f6cc3a33`

```dockerfile
```

-	Layers:
	-	`sha256:faa3b5ff4e908d54bf460ee3536702f8e6cf09361e8c632866813a483d9ac0b5`  
		Last Modified: Wed, 14 Jan 2026 18:26:01 GMT  
		Size: 40.2 KB (40231 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:0369e7401da559f75a35a0126c2f8efa7067a4a6821fbb140cfc8ea9cd91d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270596681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e187c029391a933540d24f06f8ccf9e3ab34966f97da632a809c0e7bc68cb939`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 02:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 02:40:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:41:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:41:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:41:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:47:22 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 18:48:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 18:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:49:21 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 18:49:22 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 18:49:22 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 18:49:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 18:49:23 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 18:49:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 18:49:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 18:49:23 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 18:49:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 18:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 18:53:10 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 18:53:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 18:53:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:53:11 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 18:53:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040954f92ec97ea46ab26dcebf24a6ab2cc0e67f210bcce8bcb9dfb1faf77d6`  
		Last Modified: Wed, 14 Jan 2026 02:45:56 GMT  
		Size: 3.7 MB (3710271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9425bbafe39445bfc1ee834ed06db5e9c79e7483c2092810ffa256366c90b303`  
		Last Modified: Wed, 14 Jan 2026 02:45:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1227467ea0a824b18cf8aa0feb4b8b88b12384ba6539b2279092a31ec152162`  
		Last Modified: Wed, 14 Jan 2026 17:41:36 GMT  
		Size: 33.8 MB (33835867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06452470b4f462b81916f910dcdb89d1cbe76c38cd2a514358235fa72b8c21ae`  
		Last Modified: Wed, 14 Jan 2026 17:41:29 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db8e4eabdb12d6f96b8bbe18fae0092975d100ec92b88b6870112a6157d6ca`  
		Last Modified: Wed, 14 Jan 2026 18:53:48 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c76e933a12303ce6622a209ffcb5511bb1146daf73979b62af17230192085c`  
		Last Modified: Wed, 14 Jan 2026 18:53:53 GMT  
		Size: 129.9 MB (129935334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d386e30558c7446276d0b8bc3dc582b7a01b40f5b3aab4fa4cc7f59c3206c6`  
		Last Modified: Wed, 14 Jan 2026 18:54:02 GMT  
		Size: 907.0 KB (906969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e403192a6503212e951ecbb98442f0bf8aa0257a52f8239bfd0cd5c6bf439`  
		Last Modified: Wed, 14 Jan 2026 18:54:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dabcdc95f2b2ef89594ceeca3eac34b306ef0643fb1064b064744a71b57584`  
		Last Modified: Wed, 14 Jan 2026 18:54:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fc90d89313da5aa47289897dc9ce187e19522b609e4b1cb0b47af1921d0ab3`  
		Last Modified: Wed, 14 Jan 2026 18:54:02 GMT  
		Size: 3.3 MB (3252931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2555f3105485e1ad24b892ef92683564a8244a5ffc4a0a38dcf3e1ce466e3a`  
		Last Modified: Wed, 14 Jan 2026 18:54:11 GMT  
		Size: 66.9 MB (66882484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2f9eb45e278ceac6abc8f3f7554329a06e2155360825a71fd691d2622908e`  
		Last Modified: Wed, 14 Jan 2026 03:55:55 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:cedd345c99fc01d79c221e369810fc662ecd3d8f6750b6eea4e118416d099233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa9c61cba04a21993e91d09b45be857bb96e19d6945d6abed807d04ad4578`

```dockerfile
```

-	Layers:
	-	`sha256:ad78e22d02db1dcf973b02b23cb4787ff1d9240e6a4d4677aedf1bc8b0bfaa68`  
		Last Modified: Wed, 14 Jan 2026 20:51:41 GMT  
		Size: 40.2 KB (40207 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:f123cd30d70f46413397c87ddc9caad51ee49acf1ba3ed9fbbd0c12b8262453c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250908515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447274635213da7febb8c26220e66d38ee71cc554544e8c03df7fd1d5cdb7aaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:50:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:50:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:52:03 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:52:03 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:52:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:52:03 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:52:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:52:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:52:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:52:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:52:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:52:03 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 22:42:08 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 14 Jan 2026 22:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 22:42:49 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 22:42:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 22:42:49 GMT
ENV RAILS_ENV=production
# Wed, 14 Jan 2026 22:42:49 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jan 2026 22:42:49 GMT
ENV HOME=/home/redmine
# Wed, 14 Jan 2026 22:42:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 14 Jan 2026 22:42:49 GMT
ENV REDMINE_VERSION=5.1.11
# Wed, 14 Jan 2026 22:42:49 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Wed, 14 Jan 2026 22:42:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Wed, 14 Jan 2026 22:42:49 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 14 Jan 2026 22:42:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 14 Jan 2026 22:45:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 14 Jan 2026 22:45:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jan 2026 22:45:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 22:45:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:45:02 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 14 Jan 2026 22:45:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278c74b521395e8d456670779ae7a05b6a65ebc00089ae668b5ee55ef6d62f6`  
		Last Modified: Tue, 13 Jan 2026 02:53:45 GMT  
		Size: 3.2 MB (3170974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9183b3c1e9c49337647755deafe50e320b6879585d0a54774393f706fd9fbb72`  
		Last Modified: Tue, 13 Jan 2026 02:53:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cf9879c8bb31fe509daf1e2f51cae618da1ee408555d9546b6eb016f662418`  
		Last Modified: Wed, 14 Jan 2026 17:52:33 GMT  
		Size: 33.1 MB (33105572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458db5142c4f670aed40403462b866c456aa7de6abd26bc45ef87b32189633db`  
		Last Modified: Wed, 14 Jan 2026 17:52:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb1b33b7a2e5ec7979f06cf4384e44d1ba1c97e153512b1a43149986a49eda1`  
		Last Modified: Wed, 14 Jan 2026 22:45:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c085cfa04b599768c9cf1012190f29bde45dde7bbb7c5d53db1e19d7f7d7a0`  
		Last Modified: Wed, 14 Jan 2026 22:45:51 GMT  
		Size: 118.6 MB (118623591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7a5d34f3ba30c82b466219e1039a4a3a20c6d6df945b1ee2d2993379e7a532`  
		Last Modified: Wed, 14 Jan 2026 22:45:35 GMT  
		Size: 921.1 KB (921077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403c45e81ff85424d74067b9d77b165eb9f808af34b826a2d8639b61e8f5183`  
		Last Modified: Wed, 14 Jan 2026 22:45:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f63ec756dbb59617bea606fe6ab360802381a4e5907d9b5ef6fb4faebd4e436`  
		Last Modified: Wed, 14 Jan 2026 22:45:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a60b61a784a32e7ccf0db0993d326b9316cfaca007d1831383bfefdd079f3c`  
		Last Modified: Wed, 14 Jan 2026 22:45:27 GMT  
		Size: 3.3 MB (3252924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9881df17ecb96543b9d0273420e5326eb1a1529a522e8ca3f38e0cfce0edef6d`  
		Last Modified: Wed, 14 Jan 2026 22:45:48 GMT  
		Size: 64.9 MB (64945850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb46d9a5c050a4f5414cc4ef15f58591c8a38c119407bb388f4bfa67a2b37d5e`  
		Last Modified: Wed, 14 Jan 2026 22:45:36 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:eb2f8c93efc10655f0e06a4f24a0523d536a2c3b32f1de2679b9e2e22128906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df813bb483448119f0e0ead8305ceacaf8102be59f08d430939ac0f8defe81c8`

```dockerfile
```

-	Layers:
	-	`sha256:a0dbbf5e31e8524de9e72e9d34f5f0798609c066147083bb5c754c3421ddb196`  
		Last Modified: Wed, 14 Jan 2026 23:50:26 GMT  
		Size: 40.2 KB (40158 bytes)  
		MIME: application/vnd.in-toto+json
