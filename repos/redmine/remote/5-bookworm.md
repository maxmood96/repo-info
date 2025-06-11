## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:46cfa0ab65fcb288a947f7f14feb8e8e1ff27ece5b465c200148c5a22f996f82
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
$ docker pull redmine@sha256:fbd0852db661bd2539afa4307b52d204de7c1e737b8345834f862697be83ec1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249299308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937b46a495335feaa06405abb9f1c14a0fb3690af88b3b769b1ebebbedc80402`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfa93bba0560cdbe449ef596fec402a5cff752e27b90b6db52e426eb484dc55`  
		Last Modified: Tue, 10 Jun 2025 23:51:13 GMT  
		Size: 3.5 MB (3500666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d1d08d83b6ef128abfe036d8d4676a528bdad874bdb36313500a14728c95a`  
		Last Modified: Tue, 10 Jun 2025 23:51:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1497f2646875c904b4044575b7c907456d2474740e160a12da0b26b56f8bf05`  
		Last Modified: Tue, 10 Jun 2025 23:51:14 GMT  
		Size: 36.0 MB (35958841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca2538f148b17ee266b52d4f48b6b0f13cf3ac191214ac2d133400922806fa8`  
		Last Modified: Tue, 10 Jun 2025 23:51:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e069e20faa9b57c311f394242396bf9510cab1212fbda65b468ba9ca6f380`  
		Last Modified: Wed, 11 Jun 2025 02:22:25 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d999df502b8ad399106e8bd02f85176b3fb0a9c44feb9eb7c81bc1b32d5fad`  
		Last Modified: Wed, 11 Jun 2025 04:49:53 GMT  
		Size: 122.9 MB (122939817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552e04655e3e72c7be1191183640563525d22cf8d225075d353443b8238de1f`  
		Last Modified: Wed, 11 Jun 2025 02:22:28 GMT  
		Size: 1.1 MB (1143810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae6917f0cfa3496a6c0bc369cef5cee21ffb3f2766b6829f7722597d714bf5`  
		Last Modified: Wed, 11 Jun 2025 02:22:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a287b0f1c5af10c01757b660395fee410178eb9252b170258d87c2afdd7307`  
		Last Modified: Wed, 11 Jun 2025 02:22:41 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f95349e3f029ed9812b33011554470a5b247ef65acdbd7565e8465374f9577`  
		Last Modified: Wed, 11 Jun 2025 02:22:45 GMT  
		Size: 3.2 MB (3247377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2bcfdfd02a38db46df3fba2f18ca7876aa7302ae6802063227673665f1a79`  
		Last Modified: Wed, 11 Jun 2025 04:49:49 GMT  
		Size: 54.3 MB (54274659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9c83dfc0bd8de2e98ee6c7db45f9eac2fb52ffe7892809b33e602774be997d`  
		Last Modified: Wed, 11 Jun 2025 02:24:17 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:e41274fddbad0622ca31feb04487f79b4439af549aa49a6b3627efd6bd48f44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cde3e10821aefb48ec5c8bffe0e3230919bf00586ab789b4ffe0041c78c38a`

```dockerfile
```

-	Layers:
	-	`sha256:d537cb821f5b70636bde03e98e2b9fffab0058acf25198b91e603e95f72f294f`  
		Last Modified: Wed, 11 Jun 2025 04:49:21 GMT  
		Size: 40.6 KB (40648 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:992fb1386627c59523c58838b6fdf79193b9e97345290ce3d1b35bb1fbda74d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233601350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c85bcd32e2e0352edb1d9d13a29be97de8cbd82f2e704dab3a6a4f5563a1aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
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
	-	`sha256:f0676175e83018434da61fde059309103c281414b794b17e20188c48c6031b23`  
		Last Modified: Wed, 11 Jun 2025 09:17:18 GMT  
		Size: 32.3 MB (32320396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4380bdb67f868caefab59fbfbdd06318cd9ed3931e3613aec75586543539d085`  
		Last Modified: Wed, 11 Jun 2025 06:07:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832fb362e565ea95fecbb85ef297ad0c6670242ab16c8d40161e2e3f2ab67bb1`  
		Last Modified: Wed, 11 Jun 2025 09:26:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07afafa7aba9d9e5ea069cf0105db9e2aa753c9b5e0fb704bf5fdd880d14283c`  
		Last Modified: Wed, 11 Jun 2025 09:26:43 GMT  
		Size: 116.6 MB (116585802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1c6b8f170cec0aa2411d5073d853e64ccbecacd349ac5bc6aba72d9a79f13e`  
		Last Modified: Wed, 11 Jun 2025 09:26:24 GMT  
		Size: 1.1 MB (1121236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6648838d61716f43fb9ef65ba9f7609d6c486cadaa28572d20a611b7c2d2af43`  
		Last Modified: Wed, 11 Jun 2025 09:26:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405e00cc0f1a7dece7a073f1a4756f35bbdd61f8700e6ce8f7c0cc8709cd1c89`  
		Last Modified: Wed, 11 Jun 2025 09:26:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba3f5df6a0957c85739af376f436289bdb42043db9d49dcb548778634af5ed8`  
		Last Modified: Wed, 11 Jun 2025 09:26:25 GMT  
		Size: 3.2 MB (3247373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388149be028113978bc8e6ba9a99fed668096d9ed44e86dcb50c9c76bef8ce26`  
		Last Modified: Wed, 11 Jun 2025 09:26:33 GMT  
		Size: 51.5 MB (51485594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45f3144489ff0080bbed7be7322bde0eff4075d01a157cee89a84439de7a386`  
		Last Modified: Wed, 11 Jun 2025 09:26:24 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:613c8eafc899ba53872696dfd186fc5c001c00efa9006c0628dbf5933298fbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17ec248642f44e4314bd7b77a8858a52a2144f9d77dcb9eec73577e60c4df20`

```dockerfile
```

-	Layers:
	-	`sha256:a46286b27851f5c17f46916863a9341f181b064d0d8918444fbe6c66024a582a`  
		Last Modified: Wed, 11 Jun 2025 13:49:29 GMT  
		Size: 40.8 KB (40805 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:ecd8a86fc7c86984cc33135487a16e7869293f098ae7fa93bb24dee98782a3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226680773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df0e16bbbd3e174fe384c029c08be25ecb6bc927c08387eed2aad9b845fb281`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
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
	-	`sha256:81d3052afa024d40711facff7f04d8a41d796bf4f84ac9828dbb1bf849adf54f`  
		Last Modified: Wed, 04 Jun 2025 05:46:09 GMT  
		Size: 32.2 MB (32153268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f772d9cc31ae70aa18c0cab8f08e2ca41118fb11673914d9a1e5a0321179ee`  
		Last Modified: Wed, 04 Jun 2025 05:46:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb7820850f2c3a15042d95434797b308b85380840580e948defb031ac32ae29`  
		Last Modified: Sat, 07 Jun 2025 07:05:39 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865abd864366984003ac321374b687662e7da346cfa3f815d0c1cf3fe46b25c`  
		Last Modified: Thu, 22 May 2025 16:21:51 GMT  
		Size: 112.0 MB (111995106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f866066b00fc4b9455f49925c92360cc53e2927a11d3be87a85dfe1ba76a86f`  
		Last Modified: Thu, 22 May 2025 16:21:48 GMT  
		Size: 1.1 MB (1110447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4ba4cbf8408f1768f8bba81490cddc10def55b724adbe61df5ea7e774b00b`  
		Last Modified: Sat, 07 Jun 2025 07:05:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d161a413e541fae5539f413d7c51a50a59ded89be7e1b10611455599d9add9fc`  
		Last Modified: Sat, 07 Jun 2025 07:05:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4e5f0e01f423a870ec3f757c67b938e6e21ae31af5c87a10e301971d5661e`  
		Last Modified: Thu, 22 May 2025 16:21:50 GMT  
		Size: 3.2 MB (3247370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec7fc0e1f51ff4ffeb181aa74913c36e6d3f21bd157c2a916bb30dd26a512a1`  
		Last Modified: Thu, 22 May 2025 16:21:51 GMT  
		Size: 51.3 MB (51327449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58761365ad81c8f3418e107f551a9b7fb07e96fb8f4ca11ec10005927b20552a`  
		Last Modified: Sat, 07 Jun 2025 07:05:39 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:6d6b81e78c0c1025472995659d5e0a6d1095263ac5aa125f42d1b5fc65ff5f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfe492fd99bc433e0df5880992a32f6eafeb9fe6ae80583c4dcce97800aaf0f`

```dockerfile
```

-	Layers:
	-	`sha256:aeb9b8bc31631175d9d8e20235ac1277a1217581032aa5c9c6ae8a195aa2cf10`  
		Last Modified: Wed, 11 Jun 2025 01:49:37 GMT  
		Size: 40.8 KB (40805 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:aa2b23d0b0eb1fc5cf265f4287222c135168d08609bbec7579351bfebc704bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245513853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1248567a98055f60bf2354a45f0b844c15ac91a7145f89f379b0d1a8b9905cdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
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
	-	`sha256:98b0d016cbefd1f183a6741c762a038411814f8c44cdeff5c89aab23d745767c`  
		Last Modified: Tue, 03 Jun 2025 14:07:54 GMT  
		Size: 35.9 MB (35893938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a583eb9b8ffeb88a9bddc73657225fcc4131a3cceae7ec12b494aa1e4f8c7ac`  
		Last Modified: Tue, 03 Jun 2025 14:07:51 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c89fce6a652a35df94056d999830c8b17106b5af6e3cf0db968b359dd058ba`  
		Last Modified: Tue, 03 Jun 2025 14:10:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5c21cce21eef85c1d00ef92c9fa868e14318ba37dfcc6b2cb8523ab92780c5`  
		Last Modified: Tue, 03 Jun 2025 14:10:31 GMT  
		Size: 120.2 MB (120229845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f667d3ec570e53aef61218720efe95458bcc2338d6f7a93ce78aa1bfca79ac`  
		Last Modified: Tue, 03 Jun 2025 14:10:09 GMT  
		Size: 1.1 MB (1077224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ef33f9e5681e9673efecdd8000f090b524782ad367ce552c3fad58d647d55`  
		Last Modified: Tue, 03 Jun 2025 14:10:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee3c238a4609dd4dfb78c4c42d944c39d62137e46dcbe1a504ecbf3650f88a`  
		Last Modified: Tue, 03 Jun 2025 14:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ee212df9dab5380c3f5c9b5be8688acb17fcde8133c3a4423cf4c9c14840b1`  
		Last Modified: Tue, 03 Jun 2025 14:10:09 GMT  
		Size: 3.2 MB (3247368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba962857bdadffbe563259b4d941c0459c479e72284214e848570c4a584b26`  
		Last Modified: Tue, 03 Jun 2025 14:10:17 GMT  
		Size: 53.7 MB (53671797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f852314aaaa00c116ac4dbd9d3a793f34fb49bd6050a934a3eb9e1145ff054eb`  
		Last Modified: Tue, 03 Jun 2025 14:10:08 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:a46dc4ff91be9063a89557a35c23f5249a66d6efd502f230302229b200e8fcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec7b9e8d9e131bd1eedb8659f5a4200e569bb0a2e949e7ecdc11a7a0679c922`

```dockerfile
```

-	Layers:
	-	`sha256:80cd8fecb094aa913399729ac199925ea4b392bb763e887db3607ca6672179f3`  
		Last Modified: Wed, 11 Jun 2025 01:49:41 GMT  
		Size: 40.9 KB (40851 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:109a612d8493f9f8c2386d8d94d68761cba372b74a08857cd871f979bb0f6d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247650188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f176d03ba4c9efd9a5fa47a76fbdcfbc5ffed92f352d31abe233eac30332ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733e956f86e40deb3962bbc3b15cddac48aedc779e9204b325787a7d5e656ad1`  
		Last Modified: Tue, 10 Jun 2025 23:46:48 GMT  
		Size: 3.5 MB (3506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade77fbe3f6d0949276cbe7b39b89450202adfa3c9021715508166e007267d54`  
		Last Modified: Tue, 10 Jun 2025 23:46:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc0c11678b78e5fc23bcb17d0a8a5d3be46d204bc2478e2f3732e1b69ef19d`  
		Last Modified: Tue, 10 Jun 2025 23:46:52 GMT  
		Size: 32.2 MB (32156408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c69c075e0ff7c018caf71cc16adfbe8d814888ca1671d205194a8324e0ec0f3`  
		Last Modified: Tue, 10 Jun 2025 23:46:49 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c3a51d132897213a7cdd080c4bc053b92b41ef9d659891b85292a9133cec94`  
		Last Modified: Wed, 11 Jun 2025 00:10:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e7bb74c2ab7b0404de6a017052faee2c099d5f8fd2b98b44bc5f828935f8be`  
		Last Modified: Wed, 11 Jun 2025 00:10:15 GMT  
		Size: 124.8 MB (124783090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dedb9be52736cfc790e9b3365cf4fa442975dbcac62e408b4756434f7624c31`  
		Last Modified: Wed, 11 Jun 2025 00:10:10 GMT  
		Size: 1.1 MB (1119516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97102017ffba9d16be6c6dd35ebdad2c181ca461c3e85602cc924cbe8b9be100`  
		Last Modified: Wed, 11 Jun 2025 00:10:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bfd3f22965c21af551255a38e132e11aac4d53f91dc312627d0b3c89d3c6a1`  
		Last Modified: Wed, 11 Jun 2025 00:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bf667b2efebe2a8def7ec32bd4b0a1ac547a9f53f48e1db44b95f6eba0678`  
		Last Modified: Wed, 11 Jun 2025 00:10:11 GMT  
		Size: 3.2 MB (3247380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc41a3fba18a0418de8c2d00163a9e1250fd386e86043d3abdabd6d45dabdd3f`  
		Last Modified: Wed, 11 Jun 2025 00:10:15 GMT  
		Size: 53.6 MB (53621320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ceab0a932b03e2d1175053e4a5315467c5d42c05fbc2344b3d63b11c59096b`  
		Last Modified: Wed, 11 Jun 2025 00:10:11 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:ec8cbcfa05160dbf1c5434347935000cda61e92b6796401ffa25088423b173b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be92ff2202c5ef94f7e6f32f95cd1501956d051d676bef3198ea4c73e1fccaa`

```dockerfile
```

-	Layers:
	-	`sha256:abea941bb0f96407910eed81eeae3dca639e20a361dd973e17b91788406a4eab`  
		Last Modified: Wed, 11 Jun 2025 01:49:45 GMT  
		Size: 40.6 KB (40596 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:1b0be97ad805c68619ccc22cc6c19523909530255c4a0bafe6d6fed756222359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253199461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf275eeb2bb547c892e50ece77ae1612f0713b1926165040f6e57cf2a9e903`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
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
	-	`sha256:82bb518e3ab4c44de12e1d980509d2cee3672b822e8a73be62fd65d215107bbe`  
		Last Modified: Thu, 22 May 2025 12:19:20 GMT  
		Size: 33.3 MB (33343842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d6ac0607eaaa2ddde3d0a8c46db7990b3f95ad6191e00058d42b66ecce044`  
		Last Modified: Thu, 22 May 2025 12:19:16 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f8e49996fe7816c6a9936284b366d3f9f73a22298cb58336c6123e6822b4af`  
		Last Modified: Fri, 23 May 2025 05:19:02 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec6176bfb1a2d7ee446b6302f6449dc89a6862d655d6a3761eaaa13cb5922e`  
		Last Modified: Fri, 23 May 2025 05:19:13 GMT  
		Size: 118.4 MB (118444033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2c9dd582c96dcead83fb9d25d9cb48c3cf5be2a8c854b961c4555ab8c7017f`  
		Last Modified: Fri, 23 May 2025 05:19:02 GMT  
		Size: 1.0 MB (1031189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126316a7b923a5d12a93011b2547071ec08f9ade47b088d6c3c9bb7a12d3513`  
		Last Modified: Fri, 23 May 2025 05:19:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd39b2b6e13c837b090701ca2c4d69bdfcfba3be6e15cbe6bc6d09e1720ecfa6`  
		Last Modified: Fri, 23 May 2025 05:19:03 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036a47aada684bf42eb72716e4c91c7247b58a7a760ce9dc40abc0d2279f9fd8`  
		Last Modified: Fri, 23 May 2025 05:19:03 GMT  
		Size: 3.2 MB (3247378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7aedafa195d7488ac2aa6574f0ceae3f30162424b8dae0ee9e48d7f8b89888`  
		Last Modified: Fri, 23 May 2025 05:19:10 GMT  
		Size: 65.7 MB (65719833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551a293f560bb9539e3bb5f5cd2605953acee85df116a983ae5bf9e4f62338c3`  
		Last Modified: Fri, 23 May 2025 05:19:04 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:8c9e95f9916c3881f6638eee5e69d8d431a50a3f10382799132f6a937f78b041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8167df33e8db1a3b135b94ff42fd1289e6d58548d38456057fc4f71b496fc6a5`

```dockerfile
```

-	Layers:
	-	`sha256:0b9c76b6e79c28b019487adc5c52594ee60325ba2181f489e1ce3ff8f7ba848f`  
		Last Modified: Wed, 11 Jun 2025 01:49:55 GMT  
		Size: 40.7 KB (40747 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:623f6fc501e752d11f62eb938dec0de5573c7ecb966b9baed87137201ac077eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270317800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de4f1893cc68f22c3176baedbee0a38688720cbd7b651a6bce8d30a1b7c44f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
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
	-	`sha256:5330e9ea89f0eaf09376f97abed2d9ac80f46a18ddb2b21fafdd1cec576b0d49`  
		Last Modified: Thu, 22 May 2025 10:28:12 GMT  
		Size: 33.8 MB (33827765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18392fe0a108ecc1fd23fd0434b7a15afdd9a98a3a1c9a30382a6de3d18d86f`  
		Last Modified: Thu, 22 May 2025 10:28:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475fea9b49e03d87432d25ddfefc3a6424e2fe70ffa829725b2082200feaa1e`  
		Last Modified: Thu, 22 May 2025 16:22:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c26624075eff368b6f9a0d643bed435ac0932cbade3d446bab7a2d54cf3eed`  
		Last Modified: Thu, 22 May 2025 16:22:58 GMT  
		Size: 129.9 MB (129886972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fda89ef7ffd027760348e3f7e33104563ed7433da51bd86d423b58a500b289`  
		Last Modified: Thu, 22 May 2025 16:22:55 GMT  
		Size: 1.1 MB (1066647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1354b56eff8eaaa620a4a9ce061500a6528c3262c67cba7173bf2d50950014c`  
		Last Modified: Thu, 22 May 2025 16:22:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14beb97277a74e3329aa0b3e992e5ac8853f189d95b1257901d867a080b68e2a`  
		Last Modified: Thu, 22 May 2025 16:22:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e8bb9389fcfd0ed3726c45f5fd1099adc3e7487f82fccb93252e30e950012`  
		Last Modified: Thu, 22 May 2025 16:22:56 GMT  
		Size: 3.2 MB (3247371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816fa4504e17a79cfa2bc990309e8a0ec7765792c459b9cb9e13c91c74c0c292`  
		Last Modified: Thu, 22 May 2025 16:22:59 GMT  
		Size: 66.5 MB (66513025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574f49a15fae6359cea2c8e0dc5c547c31a27d653aaf645f58af1f18ca1ec7b`  
		Last Modified: Thu, 22 May 2025 16:22:56 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:a7871213c17f8347bb37634e55bf4f69d54454a7c9a9d189c65bf745ec132707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee16cf159056f6fdbbd8ca1b563137a956caa5f68e0667f7e96a49494cecc6b3`

```dockerfile
```

-	Layers:
	-	`sha256:b9bcaa0e3ac413127fd6206e2a2b2dc670f0d4e6996491432a0584f110c48f00`  
		Last Modified: Wed, 11 Jun 2025 01:49:59 GMT  
		Size: 40.7 KB (40714 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:6a43093805bec7808b81520e9c2bccd58abfc6684383d0e588528381051ea8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250728727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23933969a8ddbbb0425166850cb4764d96db9f393e937502b89dc51889eae2c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
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
	-	`sha256:97cfe63aa1ae2923045fd7abb8a1cc6020fc28ee1e4e018103539bd2398c6722`  
		Last Modified: Wed, 11 Jun 2025 09:17:53 GMT  
		Size: 33.1 MB (33093329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b39e29e403a0102a1fb7915b52ea3f97e8cf27e18539e3539de724f93b2667`  
		Last Modified: Wed, 11 Jun 2025 06:20:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d168f63ff3bdc3ecdd434e7b409d080c7d3a50214f17e00a3fd20b9f07df111`  
		Last Modified: Wed, 11 Jun 2025 13:17:11 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3531aa65b436302a6e2a72961bee0f6f95c8cba4523db07d1c8a6cda80a5b3`  
		Last Modified: Wed, 11 Jun 2025 13:50:37 GMT  
		Size: 118.6 MB (118599322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9374a905886aaef6219cba16c88289d6c0a93a2f89c96fd61d1ab3debc4fc9b`  
		Last Modified: Wed, 11 Jun 2025 13:17:15 GMT  
		Size: 1.1 MB (1109077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c039e1946c3b454289c628ebe80e88f58fc356a2952c93b03acaef901b594415`  
		Last Modified: Wed, 11 Jun 2025 13:17:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b918e790314fe65c0267fe8a315689e92cb8b622bc4d41e39e72cd431e10073`  
		Last Modified: Wed, 11 Jun 2025 13:17:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef90d395e4d5a87960cf9c56845e0f3f63ddb5f39c670465030af041a74100a8`  
		Last Modified: Wed, 11 Jun 2025 13:17:33 GMT  
		Size: 3.2 MB (3247377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed7fdda67cf58cc8336fc0f49f1947b757573ad7515578f58f6f3eb6aa1259`  
		Last Modified: Wed, 11 Jun 2025 13:50:35 GMT  
		Size: 64.6 MB (64622842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be55019e43ff79c00c022c953c440e5f4b4cd3eedbfc2429a3909641cd825185`  
		Last Modified: Wed, 11 Jun 2025 12:25:35 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:e616f1a5d5ebf043c15e57693a620c71d1000c486edcdcdc038c3efaf2c8a22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4892f76deefd7d6b69654e252770c0ebf03422b3848ba967fab68a1f19fc99d`

```dockerfile
```

-	Layers:
	-	`sha256:3b05bccb0f49a000d6f0fc68dcb4ebf983715ab83b09c33918a46d92263f5de2`  
		Last Modified: Wed, 11 Jun 2025 13:49:41 GMT  
		Size: 40.6 KB (40648 bytes)  
		MIME: application/vnd.in-toto+json
