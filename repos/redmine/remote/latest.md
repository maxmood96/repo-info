## `redmine:latest`

```console
$ docker pull redmine@sha256:9468c853a96e03e2af57ca7295f34bae72d1b402512de68ccc5e2362f0cb3a2d
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

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:a1b85ef22842dd9334abffc3acad6a86c95b41f354b2d80d90909f0f3e3051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255108249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5503fa07260181230eb6f351cd7c2779e155dc3264219c6dd5cffacac5d5f8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f18ea0bf317f62403e40783c20554d11bd54be3cea3533767df4960f8f5b3e2`  
		Last Modified: Tue, 25 Feb 2025 02:35:12 GMT  
		Size: 3.5 MB (3499334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfd6aa30e99786ec7a9c2bd6cf559fb162adc2f479234b9aa12cf0bd0c0f216`  
		Last Modified: Tue, 25 Feb 2025 02:34:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d637d372f61e7f8db98ff68f0a1ac319c910fd0338c761b3c82ea8e5d64118`  
		Last Modified: Tue, 25 Feb 2025 02:35:12 GMT  
		Size: 37.7 MB (37712332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50509374720abfa7d9f3bdc41778e2314b55f705ab00ae82368f9869ce53603`  
		Last Modified: Tue, 25 Feb 2025 02:35:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffb63ddc8c5838583d50a5a3c80d8f06d67c39954415d46e1ba9cfaedba56f8`  
		Last Modified: Tue, 25 Feb 2025 03:22:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec3cd13c816375e805d9cf3e036a71c4ff406520a9040a3189f8837ac8ac505`  
		Last Modified: Tue, 25 Feb 2025 03:22:43 GMT  
		Size: 123.2 MB (123155024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b09615c732257da48398476a660b7690f135db64f37e69730f3f2881f580f`  
		Last Modified: Tue, 25 Feb 2025 03:22:41 GMT  
		Size: 1.1 MB (1143499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be70b66650fe7b29ca1f0b31a6f5cbecfd2c825c2151952ea4d5a19cf6b8d04`  
		Last Modified: Tue, 25 Feb 2025 03:22:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84add45e30d2a4a9ad3d0f44215018897cb5fa1de6d058d50e64e556097844a`  
		Last Modified: Tue, 25 Feb 2025 03:22:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d39d1256009bc7938eff944850b27c625c05e78bd6e10a0025ede379a731fb7`  
		Last Modified: Tue, 25 Feb 2025 03:22:42 GMT  
		Size: 4.1 MB (4053827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1354511cdac20f9b744c71a2e16469f2b8c42c8ef369df424995d269351292`  
		Last Modified: Tue, 25 Feb 2025 03:22:43 GMT  
		Size: 57.3 MB (57320922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e832ae30fbe37f3aaacd9ae9c34b573943e8ff4c8029438fe63e8ee7c87eff`  
		Last Modified: Tue, 25 Feb 2025 03:22:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:5aee5fff971c851cf439b7aae4b1e44142686d36578117efcd01e02bcac77ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01854487d7a77ffcac402cf8c424d9dd530233c17d3c80f046f37362e9053c54`

```dockerfile
```

-	Layers:
	-	`sha256:2032e861ede2df2cafe94420b3e098536edadbafb2882c12a5058501fbf3c2d9`  
		Last Modified: Tue, 25 Feb 2025 03:22:41 GMT  
		Size: 41.3 KB (41252 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:c08485e8129884e585e6a3ee622d03dea8178f10eacd7537b1913b575160f7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239515363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d1aaa29505366adf5b975b9b5521eeb38a7827eb4946e1b27e275960fea6f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91504bc1c1e71105151322b732b30225ed4af99ad052b57083b0163bea0f5f`  
		Last Modified: Tue, 04 Feb 2025 04:45:07 GMT  
		Size: 3.1 MB (3073419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d934325bc4b023af5c986fb28122fdea2b662a8442d611b55b0afdcbf5d099`  
		Last Modified: Tue, 04 Feb 2025 09:48:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6658f13980daf9c1791ae3d9d0f48ff044ec10ef26f988baa95bdad48a274541`  
		Last Modified: Sat, 15 Feb 2025 02:52:28 GMT  
		Size: 34.3 MB (34251788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757203aeeb943767d6af59a2e89c1eb2fc319b00eda1c3a7890865774f0ca6d5`  
		Last Modified: Sat, 15 Feb 2025 02:52:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baed4c3aecc537f4bcc5bc1cbca916d19d48d69a41ab139573f5420a62344c9a`  
		Last Modified: Sat, 15 Feb 2025 03:24:48 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bc19a3bfc15dc593dd6b0a394854b16e4d46ad5c7d73ae4d6c235eb12df2c1`  
		Last Modified: Sat, 15 Feb 2025 03:24:51 GMT  
		Size: 116.8 MB (116776682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ec6a10ccd966e553f06659ff619e9577b5deb2f54cecaa538ceec48f1dff3d`  
		Last Modified: Sat, 15 Feb 2025 03:24:48 GMT  
		Size: 1.1 MB (1120887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592201d61a195aa911c12a3ead37cb86905d7f817687cea53e5db27a87ad01e6`  
		Last Modified: Sat, 15 Feb 2025 03:24:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223872f3442eab8cb07d38fa927f069f4706ea7a1102672c5fd9befa820c64f`  
		Last Modified: Sat, 15 Feb 2025 03:24:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80089cae9963a72d436c55ed1ed8117c7b34bcc9b4aca136083333d870f41e70`  
		Last Modified: Sat, 15 Feb 2025 03:24:49 GMT  
		Size: 4.1 MB (4053820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1174b649c2dfdbf9129205b916ef1199a703ae724631a44e4ad4a9bae03f54c9`  
		Last Modified: Sat, 15 Feb 2025 03:24:51 GMT  
		Size: 54.5 MB (54498214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc782c6aa6a2bf0e056d52018a24116afc8a2e3cb184b26f90894be8fc1bbe`  
		Last Modified: Tue, 04 Feb 2025 11:58:49 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:e835b5e72730e9a1d14245d0503b1a0eb7a6c261e9679da0934c31f1862ec676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74410498fecdcaddc997b4e280759e187dd5419706cb5ae2c47d9a067487c08`

```dockerfile
```

-	Layers:
	-	`sha256:84921f36f3346b5f6a4e5ef74cd7135b8076b713eef5af776590e46c3579ddf2`  
		Last Modified: Sat, 15 Feb 2025 03:24:47 GMT  
		Size: 41.4 KB (41425 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:b654cc83498d40e91c5a7afe3550fd4558b08f0082ca7f04d5f6c674ac313782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232630953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d88e17d78e6f1cba907cd820a88b4f8081da5890e40f749c3b1987a8b88fa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff3d026663dffd44eec785a25c9c3855a8164799a6d4e938e18090f914a86d`  
		Last Modified: Tue, 04 Feb 2025 04:42:04 GMT  
		Size: 2.9 MB (2907810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bc87d8ba60f555c40e6f3f390b6c10cd4e09cca83480007c80cff5ac42ac81`  
		Last Modified: Tue, 04 Feb 2025 15:06:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f4b7602921b989781527a76b45df705a1d7689810b459a02c1e1b1f8bf69e5`  
		Last Modified: Sat, 15 Feb 2025 13:34:06 GMT  
		Size: 34.1 MB (34126470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98ca21063f4b1406fddf9c073e18bc6c07347382db688a9eacaa349b83ddfe2`  
		Last Modified: Sat, 15 Feb 2025 13:34:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2aef6c247a95b47ccf1aa6bc7abad0bc749f4aa268e0859b2a8787e4e49a47`  
		Last Modified: Sat, 15 Feb 2025 18:54:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc98db99922d2b87bad739f117c7195f26e9905b288d1c87f3211e11a3b81f41`  
		Last Modified: Sat, 15 Feb 2025 18:54:30 GMT  
		Size: 112.2 MB (112167976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f71356f7f0ba0413e9978ee217afb1d56e0de94514a200433c7021cc6fc367`  
		Last Modified: Sat, 15 Feb 2025 18:54:28 GMT  
		Size: 1.1 MB (1110055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4274964683068984d8f3c12046e316ab82f980402948112e64f355d2b03e17`  
		Last Modified: Sat, 15 Feb 2025 18:54:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fdee8e5ee90e5115871bbd23bfe4d079d4917cc6c4f2d147e7ee9ca4c68e10`  
		Last Modified: Sat, 15 Feb 2025 18:54:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cdc767e26fc44460e1e852f3e32b03ed9d2c08d2edd575fe0e812e6fe549a2`  
		Last Modified: Sat, 15 Feb 2025 18:54:29 GMT  
		Size: 4.1 MB (4053819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e38f28e6e2e2f9d5772ee45791774bdd13bad99f732d5839b3a1c3173faa4ca`  
		Last Modified: Sat, 15 Feb 2025 18:54:30 GMT  
		Size: 54.3 MB (54346279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026a358fe705eb682d6ff6bfe189df20bd51d2b1e62110526737ee1fec42ffa9`  
		Last Modified: Sat, 15 Feb 2025 18:54:29 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:318154b32afd0cdcc5cbedc5dd5ff1ffa31168e425187a35a78683cf94bb8114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf8ae7eb774a8bf80cc40632eaa8af22c15095fb0638b70555634c7fb95d546`

```dockerfile
```

-	Layers:
	-	`sha256:0a3b5d09f25250fd16dbb818929703182ea904fc4cea449903b0295657794b5a`  
		Last Modified: Sat, 15 Feb 2025 18:54:27 GMT  
		Size: 41.4 KB (41425 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:f57972fe523aa5da0e80a622de65603425e89e2454dc04d74d0b9e920a028022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251319643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d425489c7949ec4b2367e273d6db27b9f72c849ba61340992b08a26973e8dd96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9355eed803991b5fe9184c36a38aef87f1551a975beed62f9cedb673f825072f`  
		Last Modified: Wed, 05 Feb 2025 00:41:03 GMT  
		Size: 3.3 MB (3322828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eca120a4e9fb0e916a1ae4dd070f6046995a3b1d9d21d135c9f9b2dd6518f`  
		Last Modified: Wed, 05 Feb 2025 00:41:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a03448df48b57d1301b06177f50f344f04e6b4599daa84196ff9f26bed7a4c`  
		Last Modified: Sat, 15 Feb 2025 09:16:45 GMT  
		Size: 37.7 MB (37689465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2faab2dcfc2ec8d1f75bbf8c5bdafcd548f08dfe971db75903c9a1770c847f`  
		Last Modified: Sat, 15 Feb 2025 09:16:43 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8929b25eabbf09b1c837cc818ef780d93dbd8a363ef3761a81dff8c9aee05c89`  
		Last Modified: Sat, 15 Feb 2025 11:53:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e33c0bce2def13d34752b2891435dcd93b46df3a37b038fa9e7a744d14e994`  
		Last Modified: Sat, 15 Feb 2025 11:53:35 GMT  
		Size: 120.4 MB (120438402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9599c128e1181213589020ea14404e584d9be5e557f9bd311000dcb9a82423c1`  
		Last Modified: Sat, 15 Feb 2025 11:53:32 GMT  
		Size: 1.1 MB (1076200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7904cd986d33252871f3117f614ead19eaaae686616a0f658d147dbeb4889`  
		Last Modified: Sat, 15 Feb 2025 11:53:32 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756bd978bde4d2ac799b1d29274df7f5475bbac4f902f706a83818f952c3edb0`  
		Last Modified: Sat, 15 Feb 2025 11:53:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345697af12d34e70e9b0a3d3e4fe3fce2bf342a9870d5b259a59e94226c1d98c`  
		Last Modified: Sat, 15 Feb 2025 11:53:33 GMT  
		Size: 4.1 MB (4053813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea80ed19db0d8642ba71832a2808c60adde70488eae797caa4f7e5916b42e73`  
		Last Modified: Sat, 15 Feb 2025 11:53:35 GMT  
		Size: 56.7 MB (56694045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698e71c31c1d533f77db82695411ad375af7f0b50cd2b2f8dae510f7243149c3`  
		Last Modified: Sat, 15 Feb 2025 11:53:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:b59fc9292ca6ae1b811305e4bc8de3ed711da631d0e618c153117c41880e3fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae6e36c25186e2110c7cbba5b64e5773c8df3b93d6083a05b56a6207a1d0d66`

```dockerfile
```

-	Layers:
	-	`sha256:cb0392755e888419d975f27093cc3a1fcabf38a0aceacfbf0d357886c63edde2`  
		Last Modified: Sat, 15 Feb 2025 11:53:31 GMT  
		Size: 41.5 KB (41479 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:d3e90e28611b0ddf1b6c2acd488b0932b5d1a944a29bbda33d1abccea0c45b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254926178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119719b595d7fc73c28d8a8364f0ecae5f39dcde94e8b0f37797393870300fd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71219147d320a13e5032ed18d570878373866611758be916a4e575be6bbc4c7`  
		Last Modified: Tue, 25 Feb 2025 02:31:20 GMT  
		Size: 3.5 MB (3503462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa58ed0be7baec284e707b7c871df67d271130de3cd8f51dcd52f1b861db230`  
		Last Modified: Tue, 25 Feb 2025 02:31:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26625b78cc3004a3d1fbca431f7fe184c5e8b06b124c06341d91605354cb14f`  
		Last Modified: Tue, 25 Feb 2025 02:31:21 GMT  
		Size: 34.1 MB (34057917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f54bb224e9bb6ff311c75fc8cb5111ec0f66124b371b1a9eb9e2e08464df74`  
		Last Modified: Tue, 25 Feb 2025 02:31:20 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a221bb25fd98e72b24cb297b4d2c30e8dabbbcb1afe46fd913c3796b75e605`  
		Last Modified: Tue, 25 Feb 2025 03:21:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a057cc0e61f39bafbfe083b166395c18490e0429cdcaad018f185319d89c4554`  
		Last Modified: Tue, 25 Feb 2025 03:22:02 GMT  
		Size: 125.0 MB (125032903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca33ff2746ae0862a284a82cae6f32c32cc4bdcc26891eef91613d5ad863726a`  
		Last Modified: Tue, 25 Feb 2025 03:21:58 GMT  
		Size: 1.1 MB (1119079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f1f83400aa26d3837539b56734efdd72afe689630816357aab6fa9c3680137`  
		Last Modified: Tue, 25 Feb 2025 03:21:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94996bb7aefd082f8977aeeacf6b5730694ad3cf649df1a587d4a8e44c61b5fd`  
		Last Modified: Tue, 25 Feb 2025 03:21:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6a4a644e7cb09dd43b8ba47641c1c7c79046d8a2b0a0a1a29348efe152fb2a`  
		Last Modified: Tue, 25 Feb 2025 03:21:59 GMT  
		Size: 4.1 MB (4053819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907e76193f41e1ea8213bc83885e57a90aca177290075d7b1e49d61dfed3822`  
		Last Modified: Tue, 25 Feb 2025 03:22:01 GMT  
		Size: 58.0 MB (57960398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210a635732091478b9b8e3f02f83e8dd11a4ffa6480014b4a70afa08fede99e5`  
		Last Modified: Tue, 25 Feb 2025 03:22:00 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:8bd4cb1ab613c188a0164a40d3ad6c19269fc7a3a8080a9513f3d0caef9397ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bc21dc32f42471eac8498808cc8f77a3921e13a71ade48c92a22370a73a0ea`

```dockerfile
```

-	Layers:
	-	`sha256:fa80cd4b0364192d9b27ec1ffb682c9c17e6c8a2acd98b7a1c701b00e3da4c21`  
		Last Modified: Tue, 25 Feb 2025 03:21:58 GMT  
		Size: 41.2 KB (41190 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; mips64le

```console
$ docker pull redmine@sha256:8789aa2952aaa3dc35036a8dad2ff4e509d34e4dfe94d234fd6da726ed868768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259458704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223d4d48bcb47254e20217b1508372c46860d33b2090ec6c37d3a90c05001c56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a5ae736b15ba52070d57c9f2039f035b5f96ccbf855651ef21412c7259f474`  
		Last Modified: Tue, 04 Feb 2025 04:42:54 GMT  
		Size: 2.9 MB (2895375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86bbf1d2eff771be719b910f6d40424b5cfda05785366ae5fa7b0b5115327b7`  
		Last Modified: Wed, 05 Feb 2025 07:38:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eb539024576cb2d7658f5a538302e54c703dd9a219aebbef2e6ec122fb2356`  
		Last Modified: Sat, 15 Feb 2025 03:51:09 GMT  
		Size: 35.4 MB (35424306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9941ca4b1081492af69e127cb6cb03813f16ae92ae07e99997cffdbbdf36ae`  
		Last Modified: Sat, 15 Feb 2025 03:51:05 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fe7ab85886f016dc268cb07b96f267d022a2417c13ff429a8917a2be946b47`  
		Last Modified: Sat, 15 Feb 2025 05:01:55 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c233e6bb878c97459649b9025871b2a5850304e57635d3ae750758eea3d07a1`  
		Last Modified: Sat, 15 Feb 2025 05:02:07 GMT  
		Size: 118.6 MB (118649130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fd3d7b81a6f0a183858c30eece0761e4d78ddf9ab8134027aec647def8f0c6`  
		Last Modified: Sat, 15 Feb 2025 05:01:56 GMT  
		Size: 1.0 MB (1030823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585a7e478195b358b093df5222b8c0612ca32d3f54801a6f70c1b05bcdbc38b`  
		Last Modified: Sat, 15 Feb 2025 05:01:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd06622dac093cf37b5f21a8912ef99104c7e95ea44f7f9380aa26f06aa92e4b`  
		Last Modified: Sat, 15 Feb 2025 05:01:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aef498cddc3c0be0514d5733e4dde45f49f7a43d8ef1cc2bebfad4fda1921e`  
		Last Modified: Sat, 15 Feb 2025 05:01:58 GMT  
		Size: 4.1 MB (4053821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c720df7199a5faca5fdb3d1cf503dfdc3e20fca147dc19de530e38642b793f1e`  
		Last Modified: Sat, 15 Feb 2025 05:02:04 GMT  
		Size: 68.9 MB (68914659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfece1df2a207fdc6c08c4efc17c52f77d7c5f314d9937003177b1a73fa2bf7f`  
		Last Modified: Sat, 15 Feb 2025 05:01:58 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:c881b1e56430e53808163c5bb445a349323a0f55127883877ad6db087f61b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82ab122dee546421cb7d6d60a7eaf3628294a6df1968f6ab664ee1e80e9c22`

```dockerfile
```

-	Layers:
	-	`sha256:5a654cd1affe29e43d5dea9df389e0cba8d29a992b0639fe2e4841a22016bc1f`  
		Last Modified: Sat, 15 Feb 2025 05:01:55 GMT  
		Size: 41.4 KB (41368 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:00f8baa400b126e572a6a7996091540d59c3cdd069ca21b5068c22816cf65749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276560707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb804e462f082f7d312042a4ec17b91f41a78c35ad3960ced2899ed631b119a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebacc5e3bdcc5a17c104d34d0cb74196d470d1dfeffc22349f69a1740ad1777`  
		Last Modified: Tue, 04 Feb 2025 04:26:38 GMT  
		Size: 3.7 MB (3702957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac0a34ba0da3ca2345e7b6378db5688975309e0bffa6b78ce1c065e4ace5543`  
		Last Modified: Tue, 04 Feb 2025 11:04:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ac1488837c1220852b4e4a9a2af454c0b3dc322940d1e84fad839bfc0cccc`  
		Last Modified: Sat, 15 Feb 2025 06:28:47 GMT  
		Size: 35.8 MB (35800086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728ead5bdd5dc0bced4c79bf70b476feec2039741554bde6f15018efe4288546`  
		Last Modified: Sat, 15 Feb 2025 06:28:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5479abc899c107e0e8e9936068eb541314b70c116af82ed9a7d30d726ac5162`  
		Last Modified: Sat, 15 Feb 2025 08:45:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d20d69178056051493fbd18a15247b407ef4cab976c3ddd0546c6380bc434`  
		Last Modified: Sat, 15 Feb 2025 08:45:13 GMT  
		Size: 130.1 MB (130138978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b3f380a5a44231158e4b0847f5ae0e98a7f7cb8ac1acfca352a752c3ba8ef8`  
		Last Modified: Sat, 15 Feb 2025 08:45:09 GMT  
		Size: 1.1 MB (1066265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cc81c16fec0d8818fac9f66e83851a503d5f0254e115b45aec4385249aaea3`  
		Last Modified: Sat, 15 Feb 2025 08:45:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c66b3c4d8c3616c5ee5d12fd7c41fc8f5883df9a9e91e52627ff758c4c75cd3`  
		Last Modified: Sat, 15 Feb 2025 08:45:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49423424d940472d04fc2021ce24cbd6a5d1c061c13cf0e28d85bc4a2fd7469`  
		Last Modified: Sat, 15 Feb 2025 08:45:11 GMT  
		Size: 4.1 MB (4053821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f97658fe07d79ce469f90a6475da6fd5c0d8eb38dd54f13c2190cc572a5f1`  
		Last Modified: Sat, 15 Feb 2025 08:45:13 GMT  
		Size: 69.7 MB (69749815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb894e2d43511e3d8c5650b209a0c62db39c40a3eebf7fd05665877c04da2be`  
		Last Modified: Sat, 15 Feb 2025 08:45:11 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:e71d6a4db3b66f12a43187cf75913fb8dd1354333dfbe09b43a3efa18d73d737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199530bfa8d6f4b02537d1ca4e380c36eeaf8a8626c6390506873555e4edbb77`

```dockerfile
```

-	Layers:
	-	`sha256:059d95a281d353ac4a958546975bac93ba4391b20f8136f3eab2b0482f9cdd4b`  
		Last Modified: Sat, 15 Feb 2025 08:45:09 GMT  
		Size: 41.3 KB (41330 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:a2075871722a757c8f2c407e6d5b07ec3d1ea0dcfadfc9b7d0a94c7ba714ae9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256835394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204608b482df74d461cefe667c12574f246f82743e93fb47fcbc340dfabd282a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883a687bc74bf7b86205b797cebd7311f5b71cf92c8fd3923ed5c7c41643f944`  
		Last Modified: Tue, 04 Feb 2025 04:31:58 GMT  
		Size: 3.2 MB (3163360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166b3423d639e9126644a664dcc4959fbce7a0e973bed8621b7c10f868b678c`  
		Last Modified: Wed, 05 Feb 2025 05:44:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9907fc1da018f44f03181c321792d65b642775ca1f62da05a28314258bab4f5`  
		Last Modified: Sat, 15 Feb 2025 09:38:43 GMT  
		Size: 35.0 MB (35042356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75b12c3d4966aa3d6e86420f840bdc72637948a8218b3873f92afc5aeefb50e`  
		Last Modified: Sat, 15 Feb 2025 09:38:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40416583e7732af6f774a65923782dae0f1753cf61587679c510e56655e55f1d`  
		Last Modified: Sat, 15 Feb 2025 12:33:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc178d204125431a6c0852f85dab4cc78c030cfef649787c1bd16f086b9730`  
		Last Modified: Sat, 15 Feb 2025 12:33:24 GMT  
		Size: 118.8 MB (118819960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47292d5952bc69049c62e2dae44e02431217b3c8b2e9bb4a4c97d054b0787fd5`  
		Last Modified: Sat, 15 Feb 2025 12:33:21 GMT  
		Size: 1.1 MB (1108731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bf2df6bca2cc38b865766ba7dd0674ec0ff725a03e801ec2a263ba96f3f890`  
		Last Modified: Sat, 15 Feb 2025 12:33:21 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3475428fadb819855956cc760c90fc11c261bb67c592a03472a06d1739b485`  
		Last Modified: Sat, 15 Feb 2025 12:33:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebef2e5a59f5f2646dd75c093aa9c44909ae490aff7d48db39611f2e47e34797`  
		Last Modified: Sat, 15 Feb 2025 12:33:22 GMT  
		Size: 4.1 MB (4053824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cb98366bb941cf082bbabef6f83e09e4d64be2c68ccf13129d1982c480fd1b`  
		Last Modified: Sat, 15 Feb 2025 12:33:23 GMT  
		Size: 67.8 MB (67784528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915eb93c484850e59f257dfa36aaafa3eb1852d1740ab98bb0bea1a2a8a866f4`  
		Last Modified: Sat, 15 Feb 2025 12:33:22 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:acd890848138a3640ea44ec4c32bd4c655e46079bac6c47c64a22e30ffa10f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36df31cf68adf920dbb2a0823faf03cf66d2be8f584f69493ef2abe159ab9d64`

```dockerfile
```

-	Layers:
	-	`sha256:7ca919f4858d0c8578b36bc1c8efaaa398fc8ac7a7d6d1b7c2c81a369d579934`  
		Last Modified: Sat, 15 Feb 2025 12:33:20 GMT  
		Size: 41.3 KB (41251 bytes)  
		MIME: application/vnd.in-toto+json
