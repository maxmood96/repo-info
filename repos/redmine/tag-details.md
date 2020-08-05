<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redmine`

-	[`redmine:4`](#redmine4)
-	[`redmine:4.0`](#redmine40)
-	[`redmine:4.0.7`](#redmine407)
-	[`redmine:4.0.7-alpine`](#redmine407-alpine)
-	[`redmine:4.0.7-passenger`](#redmine407-passenger)
-	[`redmine:4.0-alpine`](#redmine40-alpine)
-	[`redmine:4.0-passenger`](#redmine40-passenger)
-	[`redmine:4.1`](#redmine41)
-	[`redmine:4.1.1`](#redmine411)
-	[`redmine:4.1.1-alpine`](#redmine411-alpine)
-	[`redmine:4.1.1-passenger`](#redmine411-passenger)
-	[`redmine:4.1-alpine`](#redmine41-alpine)
-	[`redmine:4.1-passenger`](#redmine41-passenger)
-	[`redmine:4-alpine`](#redmine4-alpine)
-	[`redmine:4-passenger`](#redmine4-passenger)
-	[`redmine:alpine`](#redminealpine)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:4`

```console
$ docker pull redmine@sha256:d6f9a8543f565f71ca837800f6ebafdc419c4df9c4ade1f51ce0e39df93e5e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4` - linux; amd64

```console
$ docker pull redmine@sha256:833e5d78c9753f2b2c13b4c69afe1cd149c5afaad67001d8a83a37b9245bc32f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216171855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809721a71330eac8df210b42075a82e9cc9dfbb2e7ff9b62c4facf44d4cecee0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2be89e251f2053dc73cf9a2bbfa3f4440486ec355fa6de5c71f570c3ed6e267c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204977614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea62738d5d1a33ebe7ecaac9ab95e1fa793b4293c4098ee771fccc0b52f68991`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:13:17 GMT
ADD file:1a4c984d1bdb683e240e8bbdfeae45b146e1f8003444ce04a84096e58a437853 in / 
# Tue, 04 Aug 2020 03:13:27 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 13:32:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 13:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 13:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 13:40:38 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 13:40:39 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 13:40:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 13:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 13:44:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 13:44:15 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 22:28:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 22:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:30:43 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 22:30:45 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 22:30:47 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 22:30:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 22:30:51 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 22:30:52 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 22:31:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 22:34:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:34:45 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 22:34:47 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 22:34:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 22:34:49 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 22:34:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4eb4ac68461c572fdc826bae247c43484a232f91f165666714ce0f5f052b0bab`  
		Last Modified: Tue, 04 Aug 2020 03:34:09 GMT  
		Size: 24.8 MB (24836059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57be01b3add2b56b4059f291cb69f93d4ac64b65e2feab72dabebf63b1dfbfa`  
		Last Modified: Tue, 04 Aug 2020 14:08:05 GMT  
		Size: 10.3 MB (10327198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ea47e08f1c51e38e7a7cf0b08773f35502d2f4c74b9dc92a213c6d4541343`  
		Last Modified: Tue, 04 Aug 2020 14:08:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db84625521961fb028a86f0a5fc28c425020900a53caad2fca6d1a76f01383`  
		Last Modified: Tue, 04 Aug 2020 14:08:39 GMT  
		Size: 20.7 MB (20713715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2617e28f0f21cfb8e35961c52cf3ffd4057ad02f2775f22a457bf035795d62`  
		Last Modified: Tue, 04 Aug 2020 14:08:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3273f22201ce403089695a6076cc590163dc2f2a8434267db3056fffc5cd8`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb2d746dedbf4eb6c0fc7b8cf24ddc2291b3c7e92cf9d177226d1162573e8b6`  
		Last Modified: Tue, 04 Aug 2020 22:43:53 GMT  
		Size: 88.7 MB (88696480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d31fb7f91b58955306a850427973eaf680db8961db69aca0c49b58c3abfac9`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.3 MB (1325699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0d2951fa1bcd46b4f5a6b6c7574d21153f4e1d81b95265569ac66c6aa1284b`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5875546d04cd4f74fb7987868f5e1e4849ee12c61736ea5018bb44a2a04049f0`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c2e8c98f73334e09c60b17bd68b19148fd7c0b3c01da9363710d5272f8f5c`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 2.7 MB (2739772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50816df5b9254ba96779634d05859aa7a60048dbb25d4b86dfcbdbfc1fde9e1`  
		Last Modified: Tue, 04 Aug 2020 22:43:34 GMT  
		Size: 56.3 MB (56334194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d81598a7a8cb7bfbc3e2a8d2a32e18cc7c29917fc0243026863d62a7524d`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:355010891af82a27986c317860885449235e7e8d4af628ad31776a97e80b9e33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198630194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4331019b9e688ec87d1a2308c17c8f53091e0e4b085da9bedad20dc8ae238459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:43:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 19:06:31 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 19:06:32 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 19:06:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 19:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 19:10:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 19:11:04 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:33:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:34:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:34:48 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:34:49 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:34:51 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:35:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:35:01 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:35:03 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:35:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:31 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:41 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa146162a26aa547ba444d6ad8434a4fa88762f3a7d212b9931a93da93c0955`  
		Last Modified: Wed, 22 Jul 2020 19:44:54 GMT  
		Size: 9.8 MB (9847867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bbbb42b38aacfb77615f8d32c153836f2560cd16be8f9784f4bf30b3255e72`  
		Last Modified: Wed, 22 Jul 2020 19:44:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f040a4b29b55a0fbe2a9df84e9c2f36295a842b928b5db4a80edb5fa27b679`  
		Last Modified: Wed, 22 Jul 2020 19:45:26 GMT  
		Size: 20.6 MB (20622549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac7fe97b91d57334860f2cb01a6a29dd0964ebf470a743b88d7c6ca7e9dd4e`  
		Last Modified: Wed, 22 Jul 2020 19:45:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dadbfb2569aadf07131e4dd990e1ac49dfee4870545964b96d0e2a1bf5678a`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a449e1e40e99de1865735d2b279524408ea1351b8aa81990c736a782b2d4210`  
		Last Modified: Thu, 23 Jul 2020 07:46:56 GMT  
		Size: 84.7 MB (84733406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02264d74f8329975abccb71909a780753b498745c9ef75b979b9529502517e9`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.3 MB (1318462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca995ec3116e6ec1195a7325e0afc9e27fb189205a4d53354ac67960ed6f838c`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ac9b3e86c9a29035edf6253f0e3df0f051c408d77c156aa6494bcb7e0e676`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c7d4aab33d80e1b177cda6b60bb5f14dc8cb2d4300fed0343206c09794fa1`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 2.7 MB (2739760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfaceadd0e490522496ccb840e68c615f0c85962e979e12a7c225344503a22c`  
		Last Modified: Thu, 23 Jul 2020 07:46:40 GMT  
		Size: 56.7 MB (56657751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112d06851090b1ca1a75df2f0d09941ee63aaf2d2b969917b7c7f8175b4f8e01`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:c9f53b0d76ea524b605ff634f7209510fcc5d894df294941146f75e0335785d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211920019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e59d16f477d6c6a2074c97fe39006d6f853ed9c6eb64165a8d3d790b01464c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:04:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:06:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:06:24 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:06:25 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:06:26 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:06:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:06:28 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:06:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:09:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:09:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:09:48 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:09:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:09:50 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:09:50 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c583882fde2e495b3f06f77cd3b3682d36bb918c14554cf30d2c7ee161dc9fb`  
		Last Modified: Thu, 23 Jul 2020 05:17:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c4fba8eefa2b46a7263602929c34e267291ef9ca03717b53c9d1f048e4b56b`  
		Last Modified: Thu, 23 Jul 2020 05:17:32 GMT  
		Size: 91.7 MB (91696457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef07d6943d1c1b05f15ae85eca86998f7750f1c35e60b76fd22d341dc35c4a2`  
		Last Modified: Thu, 23 Jul 2020 05:17:07 GMT  
		Size: 1.3 MB (1303026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab54a1ad31cd224479ac9699ee04c4c1b0f6fc19e1b92f1e6200f1efc4078e5`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc39b484b0cffbe92301f619ded4e936d75c51f602db9df2d6a50ca98f93048`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f8474208e65fa214067edf1ba7e78ee6eb8f8014f2fd712e43f1bd61f37f11`  
		Last Modified: Thu, 23 Jul 2020 05:17:05 GMT  
		Size: 2.7 MB (2739764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cd6feb09fd25ec692cfeabdcc33b943450bc7b7023d1a486512b473061da3f`  
		Last Modified: Thu, 23 Jul 2020 05:17:17 GMT  
		Size: 57.8 MB (57785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb362d000fbcd290102b537fadd3d40b9c9381049b8f6e3e4155e68bdecebd`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; 386

```console
$ docker pull redmine@sha256:f2178363f078c2aa301ca51ef99ca2eadf97d3ba954df8fad98d6728d951ca62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221021322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22cbfb1abd0184f1c39ac5d3bf265c48d40d098127ac12ae6317c47a94627a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:28:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 06:28:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 06:32:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 06:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 06:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:35:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 06:35:26 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 16:50:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 16:50:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 16:51:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:51:04 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 16:51:04 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 16:51:04 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 16:51:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 16:51:05 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 16:51:06 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 16:51:09 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 16:53:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:53:29 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 16:53:29 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 16:53:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 16:53:30 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 16:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a08c2806b9d07e191e456b4c558b5df63dd7de87f2e2b508835bbc5b74551e`  
		Last Modified: Tue, 04 Aug 2020 06:46:32 GMT  
		Size: 17.2 MB (17207416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0f87b9fa99941272a5d6e97848084b9a2e3fac033e8f975e9aed4c7687e4d`  
		Last Modified: Tue, 04 Aug 2020 06:46:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f9409304c0151340c860114b98b4afcdbf0fddf4925809919225625fa6291a`  
		Last Modified: Tue, 04 Aug 2020 06:46:43 GMT  
		Size: 20.9 MB (20884701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41b11b01ef197a4cbe56922dada1c4c9cd7d6d73775215b043968bb1092a22`  
		Last Modified: Tue, 04 Aug 2020 06:46:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97693b8301731105e8a914b2104d8e59ce5433f418755197a188bcde6af36196`  
		Last Modified: Tue, 04 Aug 2020 16:58:02 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc245d7e0ea3f04564d84cf94b177be72a6b039a756fa3cb0907352f8f1a3422`  
		Last Modified: Tue, 04 Aug 2020 16:58:34 GMT  
		Size: 94.7 MB (94730198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88ee83d219cc1dbd9f7aa390edc15772cfdc5ceca4829b80d0530e10bcd9c6`  
		Last Modified: Tue, 04 Aug 2020 16:58:04 GMT  
		Size: 1.3 MB (1337849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db434591aaf6b2104717ecc1073aaff73538a54505a7db0a5f1358dfb8818f00`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d155abeeea3550d021c1769122bb4c305d1b81366c73d13a7660111ab335ff`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c1770c1229ca1b059c643cdf10a02545db6192f0092f8a984569b91eece17b`  
		Last Modified: Tue, 04 Aug 2020 16:58:03 GMT  
		Size: 2.7 MB (2739481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925451a24c00a15b578826e1ef3d8102dd2400ec2f77334952157e4d81ac05c8`  
		Last Modified: Tue, 04 Aug 2020 16:58:16 GMT  
		Size: 56.4 MB (56366844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e593ee226ab0b438ea9e0653a6a8106aa816dd64eed2d2670c2464f9f00462`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; mips64le

```console
$ docker pull redmine@sha256:cf580d908948f74b725b71af887645cfedb9fc589b3b32dc0708e56c92679dbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210450731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d78379974db691acab79ddb59be559e9424fefa68da382ccdf36edab08da9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:23 GMT
ADD file:4164c71b841ba2c1f213c9fdc073ec3d4c7d79dadfcd9d771768750a3085d616 in / 
# Tue, 04 Aug 2020 06:42:24 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 14:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:28:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 14:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 14:36:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:36:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 14:36:43 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 23:36:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 23:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:38:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:38:16 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 23:38:16 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 23:38:16 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 23:38:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 23:38:18 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 23:38:19 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 23:38:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 23:44:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:44:05 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 23:44:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 23:44:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 23:44:06 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 23:44:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1333f76e75c0136aa2eb56b14271ef57d1f975f40fe2a56536d99b7c86c3aa29`  
		Last Modified: Tue, 04 Aug 2020 06:48:41 GMT  
		Size: 25.8 MB (25762724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db62010f6d33693e293c6f7e1f4a0ac8e25f991148111fd59ae56c62b6fb2952`  
		Last Modified: Tue, 04 Aug 2020 14:54:45 GMT  
		Size: 11.6 MB (11607928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4141050c0e58a8dddd238c62fd70b025302a9c8e8865cebf001dfebbb7c93b`  
		Last Modified: Tue, 04 Aug 2020 14:54:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d803382aa266318dfb2a52503c0eeb55d5fe9de18b3fbe835a9afbca7c0073d`  
		Last Modified: Tue, 04 Aug 2020 14:55:44 GMT  
		Size: 21.6 MB (21637848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3573e3ba846080432ddd673ddf9e5d802402ce3918ba7053368c28e01a963f5`  
		Last Modified: Tue, 04 Aug 2020 14:55:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcfb33ccf8f0380aa1d0b7f352cf240cf8df786b91de8d80306db3153f7d12`  
		Last Modified: Tue, 04 Aug 2020 23:53:39 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dad1bd5ce73a7a970dc0d953cc42236f7ffa5b528a6af0eaa234586c3335bb`  
		Last Modified: Tue, 04 Aug 2020 23:54:46 GMT  
		Size: 90.1 MB (90079123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43391042277f010d07116bcaf9e1aa4c325dc2c50dee6011fa8e7e1085e7edd9`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 1.3 MB (1256601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99da4257b265b0c9fa53948454fc184f3e851a1f1ac4b5aa67a678c66d265860`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf806cf56575cea106d5e3ebc5168d3f3cf7c52431d69fc1739e4f7c69e72f3`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a385f169e3df2bd1f65afc062b46112b75ee76f0fd39fdbb067ca743fc884a`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 2.7 MB (2739480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913c98a27840a8b69cdf53041383bce1fe2d778f91983aed82a9ed39d37061fc`  
		Last Modified: Tue, 04 Aug 2020 23:54:08 GMT  
		Size: 57.4 MB (57362619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b052041f3ba260c6a5fd48151a512025362178e7dc882f6959b65597602d8`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; ppc64le

```console
$ docker pull redmine@sha256:470af361a42a77d0c7ef84e405dcc86d264fd7ce9e7767bac317d396848f30ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227983214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619b68c811c421da7ad2e9e7b5c67de5f6a2a08b7dc0514ea681f2e65fac321`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:58:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:58:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 16:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 17:13:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 17:13:57 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 17:14:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 17:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 17:27:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 17:28:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 17:28:20 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:05:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:11:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:12:03 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:12:11 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:12:13 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:12:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:12:31 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:12:38 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:12:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:18:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:18:53 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:18:56 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:19:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:19:10 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:19:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4350e6f81db330ef296d21f9c43861e1d84a7979a7ab436c900ca40df5b93`  
		Last Modified: Wed, 22 Jul 2020 17:48:57 GMT  
		Size: 12.7 MB (12687936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b65160a4a21d5c38f87822df4ee82ca8a11f8b3785ea2120b3392402bf258a`  
		Last Modified: Wed, 22 Jul 2020 17:48:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6597f444d557392effc8b79dbf2c232ba5d941ebe724fa6249cf776cc29cf8`  
		Last Modified: Wed, 22 Jul 2020 17:49:48 GMT  
		Size: 22.0 MB (21970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a2a282b34bc40aad20adf0e7e9c38cad7b1a6855b7ec10705458b8d866a24`  
		Last Modified: Wed, 22 Jul 2020 17:49:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb3cce1a71287b14e02351ac19beaf109278c759f26ab033ea5d621320bba54`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f236001c13bbc805a1e4713ad6c5ed0e476464eacdfd44ba608a418c1877d007`  
		Last Modified: Thu, 23 Jul 2020 05:41:12 GMT  
		Size: 100.3 MB (100344362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aead886d739bd3bc027292813e19b942521fd83e2b87b84d7ffc57cf359fd04d`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.3 MB (1290010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf6afd72f85c187c4e3cd56894c0bd2fc5342847b64e204b8380d74572930c`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c518dbadfc9a2b2040e19141f943668ca44272fa3522b735d8d40966dcc238bc`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b813ca710fb3e9cf25dea3c2473a35f4165a8c4d1cb4e3c1209547b4b1da26ce`  
		Last Modified: Thu, 23 Jul 2020 05:40:47 GMT  
		Size: 2.7 MB (2739767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927698c2c46c1e2009a7d99151cb2489579f4c2d2c6b43be64618a6915bff86`  
		Last Modified: Thu, 23 Jul 2020 05:40:55 GMT  
		Size: 58.4 MB (58421593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b0e2e590831a782eae54596172a684f302529c2726b8e70b6136621a7dcc83`  
		Last Modified: Thu, 23 Jul 2020 05:40:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; s390x

```console
$ docker pull redmine@sha256:9cacc436f5e29968b595f56a05fb9a85d8cf599ad03ff9e513f249d68d9e2b1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210720601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84be3ab4689f85e4e730235b2d5605c6aed59471c02fa85ef7d8370f46a85d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:26:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 05:26:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 05:38:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 05:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:38:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 05:38:37 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 11:06:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 11:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:07:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:07:31 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 11:07:31 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 11:07:32 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 11:07:33 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 11:07:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 11:09:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:09:19 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 11:09:19 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 11:09:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 11:09:19 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 11:09:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e211a076d7bec7a39d1bc35ccd2ecfb97ecad9d15942b454d420c015aec78`  
		Last Modified: Tue, 04 Aug 2020 05:43:18 GMT  
		Size: 10.8 MB (10796400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea16a6f63db965daa21205a21bc3d56b39bc5415cb4fc0fbd4adc06bf68dbf`  
		Last Modified: Tue, 04 Aug 2020 05:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652803a9a3f37b5c0eb597d3cb545de4faeb3c8a0777c699a3b469318679edfc`  
		Last Modified: Tue, 04 Aug 2020 05:43:40 GMT  
		Size: 21.6 MB (21597298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661376aa0be2fb0f0f21b27678f8b46875aae059d564c4315df9156902b3fc58`  
		Last Modified: Tue, 04 Aug 2020 05:43:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9663cc42a0bb2db620a9f95bf2eac90ab8bb99edc3270b24130730ac855079`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4fee1c0fdf6aa4e3bdf1ad574569cc4b91918ecccf3121781b6222a536c493`  
		Last Modified: Tue, 04 Aug 2020 11:13:14 GMT  
		Size: 90.9 MB (90854185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a738a595cfdd936a270ac3a839188391d9a832eb23a682df205b380edef952`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.4 MB (1355115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4ded94c32cc1762576dc5d1895c8ff2a61981a4b18f844ab529a5bc3f11a60`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4fc727b1933c0c8e1ec90802948f0caa3068693f5edc86e07fc249ba40c9c7`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9d70d6ba3b29079423c01dae21a4f44b5de6687dc28b84909413ddf4de164f`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.7 MB (2739769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5248a897bfb0f149c6c341f108ecccd52d07ffd97ed1aeea3bf0872bf4654f`  
		Last Modified: Tue, 04 Aug 2020 11:13:05 GMT  
		Size: 57.7 MB (57665687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaad00d5183f9814d6f3c76d671245eff35857f941e9587960a79408ae0116e`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0`

```console
$ docker pull redmine@sha256:2d7c25f873078ca1e60b736ea317332a16db8cb30b06c381cdc9e21043d40eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.0` - linux; amd64

```console
$ docker pull redmine@sha256:dde83c4915d56b1199e55c40649a846aa3a3b1a9296aa5d80cc1a3bf20c38906
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206061894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370521b17b3bfbf20d3467c8e2814ff2d72b9ec6a86e7fa4a1215f6cec32aea4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:39:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:56 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:39:56 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:39:56 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:39:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 07:40:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:42:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:42:15 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:42:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:42:16 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:42:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8421586d2cf63ecabb151095d53b7cc8a0d95a541b637313934d75701073d8e8`  
		Last Modified: Thu, 23 Jul 2020 07:43:53 GMT  
		Size: 80.2 MB (80200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1929ed7d3aeaa2c591151007973952a2665927e96155eac2493213095926d28b`  
		Last Modified: Thu, 23 Jul 2020 07:43:38 GMT  
		Size: 1.4 MB (1355992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f456cc6dd350a548741d36e834080e66862d12b35417e17cc6902bb2bad3065a`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f00e083cd2f3e056a2eca08b9c178cf998b0037a3117bfb8b1b2ffea614eb3`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a07e8dbc83b379142ab0610272789c07e7f137ebce010d7583561127873864f`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.5 MB (2535009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7759132941903777b7330a16aab22d0a1f1cec0454f6f147101486703c3ff`  
		Last Modified: Thu, 23 Jul 2020 07:43:46 GMT  
		Size: 60.9 MB (60877903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ef7df94104fcf347bbbe2c87b1b27db67b72b15808224c5a0eeff915e8f58`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v5

```console
$ docker pull redmine@sha256:5cab9624d246de64a25b5a0643c3699eb7298d83bd724717a6cd5921361f84a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195786178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0551077dcdc64cb5d9d10adb8de7d142ff251ed6eee57cf390321418fdaf65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:13:17 GMT
ADD file:1a4c984d1bdb683e240e8bbdfeae45b146e1f8003444ce04a84096e58a437853 in / 
# Tue, 04 Aug 2020 03:13:27 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 13:32:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 13:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 13:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 13:40:38 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 13:40:39 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 13:40:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 13:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 13:44:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 13:44:15 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 22:28:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 22:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:36:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:36:54 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 22:36:57 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 22:36:57 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 22:37:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 22:37:08 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 22:37:08 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 22:37:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 22:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:42:52 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 22:42:53 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 22:42:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 22:42:57 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 22:42:59 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4eb4ac68461c572fdc826bae247c43484a232f91f165666714ce0f5f052b0bab`  
		Last Modified: Tue, 04 Aug 2020 03:34:09 GMT  
		Size: 24.8 MB (24836059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57be01b3add2b56b4059f291cb69f93d4ac64b65e2feab72dabebf63b1dfbfa`  
		Last Modified: Tue, 04 Aug 2020 14:08:05 GMT  
		Size: 10.3 MB (10327198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ea47e08f1c51e38e7a7cf0b08773f35502d2f4c74b9dc92a213c6d4541343`  
		Last Modified: Tue, 04 Aug 2020 14:08:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db84625521961fb028a86f0a5fc28c425020900a53caad2fca6d1a76f01383`  
		Last Modified: Tue, 04 Aug 2020 14:08:39 GMT  
		Size: 20.7 MB (20713715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2617e28f0f21cfb8e35961c52cf3ffd4057ad02f2775f22a457bf035795d62`  
		Last Modified: Tue, 04 Aug 2020 14:08:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3273f22201ce403089695a6076cc590163dc2f2a8434267db3056fffc5cd8`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745d6281cbab021152a30a4f6a353de13a21afb89552dcf2160257231622db63`  
		Last Modified: Tue, 04 Aug 2020 22:44:32 GMT  
		Size: 76.1 MB (76068284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1b9f5c3a4ffac38d0a36f0812063989e9e3cde1d4e82e6994c21a4b96ea08a`  
		Last Modified: Tue, 04 Aug 2020 22:44:08 GMT  
		Size: 1.3 MB (1314455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a371ca736eba3549aa02c7e837ab49104b1afc4b44cbbc06250d484378261c`  
		Last Modified: Tue, 04 Aug 2020 22:44:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e127a12494320c40b94686198f6d2eb3b05f99e7e38654fa0a2b966a5c78ed`  
		Last Modified: Tue, 04 Aug 2020 22:44:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa316b9187303a8bc9ec9b043776265c0b65caeb7e939e2355e7a22d0b33784`  
		Last Modified: Tue, 04 Aug 2020 22:44:07 GMT  
		Size: 2.5 MB (2535497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac12512db30c830589b2a42d0b2d891495b0e11c51835408ab1974187f000538`  
		Last Modified: Tue, 04 Aug 2020 22:44:21 GMT  
		Size: 60.0 MB (59986475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafdc3e57183a2612dace8a7ae7c7a8eb4be9776ed1d71c32d5a84bec84ddff4`  
		Last Modified: Tue, 04 Aug 2020 22:44:05 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c59c4cc19a61c10649637e26f61a8930a50af6703484fc03ddf11368fad0c1c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189134427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69a4639534cf392cb46605575073f17323ccc5f1e6da0dcae6cd5b3e849d4d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:43:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 19:06:31 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 19:06:32 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 19:06:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 19:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 19:10:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 19:11:04 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:33:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:40:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:40:44 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:40:47 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:40:51 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:41:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:41:11 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 07:41:13 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 07:41:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:46:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:46:07 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:46:09 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:46:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:46:13 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:46:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa146162a26aa547ba444d6ad8434a4fa88762f3a7d212b9931a93da93c0955`  
		Last Modified: Wed, 22 Jul 2020 19:44:54 GMT  
		Size: 9.8 MB (9847867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bbbb42b38aacfb77615f8d32c153836f2560cd16be8f9784f4bf30b3255e72`  
		Last Modified: Wed, 22 Jul 2020 19:44:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f040a4b29b55a0fbe2a9df84e9c2f36295a842b928b5db4a80edb5fa27b679`  
		Last Modified: Wed, 22 Jul 2020 19:45:26 GMT  
		Size: 20.6 MB (20622549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac7fe97b91d57334860f2cb01a6a29dd0964ebf470a743b88d7c6ca7e9dd4e`  
		Last Modified: Wed, 22 Jul 2020 19:45:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dadbfb2569aadf07131e4dd990e1ac49dfee4870545964b96d0e2a1bf5678a`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e0ea13aded1ce7251ad1a588080b1590f55b6ce64dc589ca9c0f043b482a54`  
		Last Modified: Thu, 23 Jul 2020 07:47:31 GMT  
		Size: 72.4 MB (72395846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e4eab866c4673d501aabad3ad5d808a07e590177f6ef10797db3596d7143ee`  
		Last Modified: Thu, 23 Jul 2020 07:47:07 GMT  
		Size: 1.3 MB (1304755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3573d010a5c2764f16d0e17c1e2b345fdcb92512cf18bb837efd994f00cf6621`  
		Last Modified: Thu, 23 Jul 2020 07:47:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1210f2f871d5bb715127e1b4ef42539822daff409a5a2063870a154abcf0d0f3`  
		Last Modified: Thu, 23 Jul 2020 07:47:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46939e830ced4e6374ad9bb78ae0044cf72b1a18ec4d5078575c58f5cd9a5542`  
		Last Modified: Thu, 23 Jul 2020 07:47:07 GMT  
		Size: 2.5 MB (2535507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e2898190dc09b95919da12934cbc47735cf56c9e7255195e7ba57597f0057`  
		Last Modified: Thu, 23 Jul 2020 07:47:20 GMT  
		Size: 59.7 MB (59717504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fe19b033c047b35a8c7fef3c66730c2b2445bd93fd17a7f2680d528a72a3b7`  
		Last Modified: Thu, 23 Jul 2020 07:47:05 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:8b9e592a28ab4b471f70df267d23bdb84ec8561a4649451922c5ab4319863944
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201860787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb23fe305418ef2cb1fc2e91109586c5c6927570cdd7dfa30afeca278213b5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:04:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:11:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:11:30 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:11:32 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:11:33 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:11:45 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 05:11:45 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 05:11:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:16:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:16:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:16:45 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:16:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:16:47 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:16:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c583882fde2e495b3f06f77cd3b3682d36bb918c14554cf30d2c7ee161dc9fb`  
		Last Modified: Thu, 23 Jul 2020 05:17:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c6e657542c66457d71773dc51409426a6c3c3e3850ff5ea5fef89042e89676`  
		Last Modified: Thu, 23 Jul 2020 05:18:05 GMT  
		Size: 78.8 MB (78833310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b83213c7c100025a12ed80c1565f69a2427307ceea82b70d3ab5e6b3ceeb90`  
		Last Modified: Thu, 23 Jul 2020 05:17:43 GMT  
		Size: 1.3 MB (1290975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59856d8208959620184862c438f36607210d3ef5de0bda3575b1147a0d1269e0`  
		Last Modified: Thu, 23 Jul 2020 05:17:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a884d9e13e73bc85d00ecac3427c840d0eae24533e954cfe0fc2c46ed0e1741`  
		Last Modified: Thu, 23 Jul 2020 05:17:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db6b4272221685420fbcf78ccdfdd7240f8015e60ee23878f31c867d10fdb67`  
		Last Modified: Thu, 23 Jul 2020 05:17:42 GMT  
		Size: 2.5 MB (2535505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0d724ceac8ee7ae4d7ebab40475ada35b3dfb0643174ccaf68480d680cbe88`  
		Last Modified: Thu, 23 Jul 2020 05:17:54 GMT  
		Size: 60.8 MB (60805476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2543b1f1de3ac2367b6c5f6d164bbec6e191316699163fbadf3a92e669e0032e`  
		Last Modified: Thu, 23 Jul 2020 05:17:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; 386

```console
$ docker pull redmine@sha256:fdee3f956688156989378eaa8b4bf13e458a853437e9dbfa0d93a69213077a70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211342322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deeed82a74dea306f67d0f77eadfc814c63d1ed4f3c8b733ce5b95937d24b1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:28:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 06:28:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 06:32:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 06:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 06:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:35:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 06:35:26 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 16:50:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 16:54:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 16:54:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:54:17 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 16:54:17 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 16:54:18 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 16:54:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 16:54:19 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 16:54:19 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 16:54:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 16:57:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:57:39 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 16:57:39 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 16:57:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 16:57:39 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 16:57:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a08c2806b9d07e191e456b4c558b5df63dd7de87f2e2b508835bbc5b74551e`  
		Last Modified: Tue, 04 Aug 2020 06:46:32 GMT  
		Size: 17.2 MB (17207416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0f87b9fa99941272a5d6e97848084b9a2e3fac033e8f975e9aed4c7687e4d`  
		Last Modified: Tue, 04 Aug 2020 06:46:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f9409304c0151340c860114b98b4afcdbf0fddf4925809919225625fa6291a`  
		Last Modified: Tue, 04 Aug 2020 06:46:43 GMT  
		Size: 20.9 MB (20884701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41b11b01ef197a4cbe56922dada1c4c9cd7d6d73775215b043968bb1092a22`  
		Last Modified: Tue, 04 Aug 2020 06:46:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97693b8301731105e8a914b2104d8e59ce5433f418755197a188bcde6af36196`  
		Last Modified: Tue, 04 Aug 2020 16:58:02 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16eed1d52f4ec29adbba4179d05ddea3800526a5fc29ec3be578faf08a445b6a`  
		Last Modified: Tue, 04 Aug 2020 16:59:05 GMT  
		Size: 81.6 MB (81645618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1a7365bcd00e37a029c64d5dc15bf6394735dc4cd6f5dadb52f1bbd631264`  
		Last Modified: Tue, 04 Aug 2020 16:58:42 GMT  
		Size: 1.3 MB (1326640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3334b58d340de03ebd03a1ec01f8254b20c119eed16b5761981c7de11d8da56`  
		Last Modified: Tue, 04 Aug 2020 16:58:40 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cab8f6188c58f0cd59c66a11d49f1f46041aa57f14a4ac3c795dad2ba9f0f9`  
		Last Modified: Tue, 04 Aug 2020 16:58:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54b2b38a5fd342820711e6273489b662db69cde3fc20725f6c327dcf46b8a8`  
		Last Modified: Tue, 04 Aug 2020 16:58:42 GMT  
		Size: 2.5 MB (2535010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a41b56de95f92c387c06cd44f0546383e4a2d2659098494a1a85eb9bf3a1cb`  
		Last Modified: Tue, 04 Aug 2020 16:58:56 GMT  
		Size: 60.0 MB (59988104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da96670b5aa1e721e7d20289c5cb5afcbac64a310102772d6fa98869eb804e7`  
		Last Modified: Tue, 04 Aug 2020 16:58:40 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; mips64le

```console
$ docker pull redmine@sha256:0993e946e6f2bdcc4a565fb80f1f947c29c7cd1578398f66e06919f392eb20ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201070243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60083ce34e151b154db3f0d5014a505d68bd01e06ba2a52fba3a5cf57bd9e1e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:23 GMT
ADD file:4164c71b841ba2c1f213c9fdc073ec3d4c7d79dadfcd9d771768750a3085d616 in / 
# Tue, 04 Aug 2020 06:42:24 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 14:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:28:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 14:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 14:36:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:36:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 14:36:43 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 23:36:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 23:45:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:45:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:45:42 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 23:45:42 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 23:45:43 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 23:45:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 23:45:45 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 23:45:45 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 23:45:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 23:53:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:53:24 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 23:53:24 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 23:53:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 23:53:25 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 23:53:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1333f76e75c0136aa2eb56b14271ef57d1f975f40fe2a56536d99b7c86c3aa29`  
		Last Modified: Tue, 04 Aug 2020 06:48:41 GMT  
		Size: 25.8 MB (25762724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db62010f6d33693e293c6f7e1f4a0ac8e25f991148111fd59ae56c62b6fb2952`  
		Last Modified: Tue, 04 Aug 2020 14:54:45 GMT  
		Size: 11.6 MB (11607928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4141050c0e58a8dddd238c62fd70b025302a9c8e8865cebf001dfebbb7c93b`  
		Last Modified: Tue, 04 Aug 2020 14:54:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d803382aa266318dfb2a52503c0eeb55d5fe9de18b3fbe835a9afbca7c0073d`  
		Last Modified: Tue, 04 Aug 2020 14:55:44 GMT  
		Size: 21.6 MB (21637848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3573e3ba846080432ddd673ddf9e5d802402ce3918ba7053368c28e01a963f5`  
		Last Modified: Tue, 04 Aug 2020 14:55:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcfb33ccf8f0380aa1d0b7f352cf240cf8df786b91de8d80306db3153f7d12`  
		Last Modified: Tue, 04 Aug 2020 23:53:39 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a736ce956d735192f44776c18fbfe2408e92a7b047e9b25bcc64b7ba217b49ce`  
		Last Modified: Tue, 04 Aug 2020 23:56:02 GMT  
		Size: 77.3 MB (77335293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5eef2396d0ce929b48256d919b7730bf5189e092a9cfd6a5c5782ce863934`  
		Last Modified: Tue, 04 Aug 2020 23:55:06 GMT  
		Size: 1.2 MB (1243184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeb51a2d1ea443d8d42fdd6bc6cf701e6e5d9aac1a97fdf3824dc2f5d295829`  
		Last Modified: Tue, 04 Aug 2020 23:55:02 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65858becdd1b7f8143f8ae95f83db55157e98ac9152f4e71bc41cc75bc5951ea`  
		Last Modified: Tue, 04 Aug 2020 23:55:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6351cf7a6080611e4938d3386c169026405e0c06ddf29990756549b80f7e87e4`  
		Last Modified: Tue, 04 Aug 2020 23:55:06 GMT  
		Size: 2.5 MB (2535008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd4cc34a24ea0bb6dcbba956ab8b0b7d6efbbd89c99d88883446587e7c6b3b5`  
		Last Modified: Tue, 04 Aug 2020 23:55:37 GMT  
		Size: 60.9 MB (60943848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c3790e650538acdb203f6ddd1753491eb41c35e07122986031fc2fdc262eb9`  
		Last Modified: Tue, 04 Aug 2020 23:55:02 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; ppc64le

```console
$ docker pull redmine@sha256:19967cb5483ba88ac9ee1a1ef8a55c57bfbca7dfb8f52bb96e1c309a13cac79c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217402766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0b1c442629c27db425c65556e85a0f51cf6cf173d233cfa6599077d43a3c20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:58:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:58:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 16:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 17:13:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 17:13:57 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 17:14:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 17:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 17:27:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 17:28:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 17:28:20 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:05:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:25:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:25:08 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:25:11 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:25:16 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:25:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:25:37 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 05:25:40 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 05:25:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:39:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:39:56 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:40:01 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:40:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:40:09 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:40:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4350e6f81db330ef296d21f9c43861e1d84a7979a7ab436c900ca40df5b93`  
		Last Modified: Wed, 22 Jul 2020 17:48:57 GMT  
		Size: 12.7 MB (12687936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b65160a4a21d5c38f87822df4ee82ca8a11f8b3785ea2120b3392402bf258a`  
		Last Modified: Wed, 22 Jul 2020 17:48:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6597f444d557392effc8b79dbf2c232ba5d941ebe724fa6249cf776cc29cf8`  
		Last Modified: Wed, 22 Jul 2020 17:49:48 GMT  
		Size: 22.0 MB (21970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a2a282b34bc40aad20adf0e7e9c38cad7b1a6855b7ec10705458b8d866a24`  
		Last Modified: Wed, 22 Jul 2020 17:49:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb3cce1a71287b14e02351ac19beaf109278c759f26ab033ea5d621320bba54`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e37e0be64b990addd251d0f9fdddeb87e20d72f84ebbba46ac3c28cbb2e216`  
		Last Modified: Thu, 23 Jul 2020 05:41:57 GMT  
		Size: 86.9 MB (86921419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2334ed06b483d738150dba7c7158c4f2854df32a02bc51464aec28882a179a29`  
		Last Modified: Thu, 23 Jul 2020 05:41:37 GMT  
		Size: 1.3 MB (1275771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062d640f81f37c02f7709d4b7f1c04d8f5820c40c0eb9575fa276afc5850242c`  
		Last Modified: Thu, 23 Jul 2020 05:41:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180999f24c7cccb8123968a2fa570afc8118c61a97950389328b9cd9a92656a`  
		Last Modified: Thu, 23 Jul 2020 05:41:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167975fda242188d5b0a0339cd2cf2187794dbc9eb6117ee2d134d696b41d07e`  
		Last Modified: Thu, 23 Jul 2020 05:41:31 GMT  
		Size: 2.5 MB (2535507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beed388de79a2865aa2236ac9d617bcde66eb81f6088fa45be01a46d97a338c4`  
		Last Modified: Thu, 23 Jul 2020 05:41:41 GMT  
		Size: 61.5 MB (61482589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb946c71e2ef4b1796f33380f85c1ea907e76248fbafc042b41d1efb5764c32b`  
		Last Modified: Thu, 23 Jul 2020 05:41:31 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; s390x

```console
$ docker pull redmine@sha256:a7d1d37430b4ab8bae6c6f3852e734208beeb4d2b9e3583f4a96f26d9d118426
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201288284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0fb07952267e3d0f167632ad977484cfc3afbc1e2ab4184c5e58dda9fd0ece`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:26:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 05:26:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 05:38:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 05:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:38:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 05:38:37 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 11:06:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 11:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:10:00 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 11:10:00 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 11:10:00 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 11:10:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 11:10:01 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 11:10:01 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 11:10:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 11:12:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:12:31 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 11:12:31 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 11:12:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 11:12:32 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 11:12:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e211a076d7bec7a39d1bc35ccd2ecfb97ecad9d15942b454d420c015aec78`  
		Last Modified: Tue, 04 Aug 2020 05:43:18 GMT  
		Size: 10.8 MB (10796400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea16a6f63db965daa21205a21bc3d56b39bc5415cb4fc0fbd4adc06bf68dbf`  
		Last Modified: Tue, 04 Aug 2020 05:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652803a9a3f37b5c0eb597d3cb545de4faeb3c8a0777c699a3b469318679edfc`  
		Last Modified: Tue, 04 Aug 2020 05:43:40 GMT  
		Size: 21.6 MB (21597298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661376aa0be2fb0f0f21b27678f8b46875aae059d564c4315df9156902b3fc58`  
		Last Modified: Tue, 04 Aug 2020 05:43:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9663cc42a0bb2db620a9f95bf2eac90ab8bb99edc3270b24130730ac855079`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07fbc7f0b2c4d4775f04fc7905722382aae9f503f30f6030e2eed8d85270293`  
		Last Modified: Tue, 04 Aug 2020 11:13:36 GMT  
		Size: 78.0 MB (77994752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bfb4ff00ef224f9003e27cbcb18cb2ceb68336c296173733770fb7292751d`  
		Last Modified: Tue, 04 Aug 2020 11:13:24 GMT  
		Size: 1.3 MB (1341792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632ad4b8a18acf543f13be6e341751e47b2d7c00bd3211efcff163ab6151bf7f`  
		Last Modified: Tue, 04 Aug 2020 11:13:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41c99ae0ddfbca193f8a35aebe77c61875b120da82d79bd9a3e11f70bad1c0`  
		Last Modified: Tue, 04 Aug 2020 11:13:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af22ef0a88d31b5c3e9b3084ddb80193cd77fccbe7b028d1f2a97d56eee1ee0`  
		Last Modified: Tue, 04 Aug 2020 11:13:23 GMT  
		Size: 2.5 MB (2535500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daa9f5c6767131d8df43ee05ad7c4cd4d4520b3a87200644902578c66c6291d`  
		Last Modified: Tue, 04 Aug 2020 11:13:29 GMT  
		Size: 61.3 MB (61310395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c182e03ed6ba8c148b60999836d2c27ef64d919853de976bb7bb250e0ca6dfe1`  
		Last Modified: Tue, 04 Aug 2020 11:13:23 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.7`

```console
$ docker pull redmine@sha256:2d7c25f873078ca1e60b736ea317332a16db8cb30b06c381cdc9e21043d40eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.0.7` - linux; amd64

```console
$ docker pull redmine@sha256:dde83c4915d56b1199e55c40649a846aa3a3b1a9296aa5d80cc1a3bf20c38906
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206061894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370521b17b3bfbf20d3467c8e2814ff2d72b9ec6a86e7fa4a1215f6cec32aea4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:39:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:56 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:39:56 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:39:56 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:39:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 07:40:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:42:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:42:15 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:42:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:42:16 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:42:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8421586d2cf63ecabb151095d53b7cc8a0d95a541b637313934d75701073d8e8`  
		Last Modified: Thu, 23 Jul 2020 07:43:53 GMT  
		Size: 80.2 MB (80200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1929ed7d3aeaa2c591151007973952a2665927e96155eac2493213095926d28b`  
		Last Modified: Thu, 23 Jul 2020 07:43:38 GMT  
		Size: 1.4 MB (1355992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f456cc6dd350a548741d36e834080e66862d12b35417e17cc6902bb2bad3065a`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f00e083cd2f3e056a2eca08b9c178cf998b0037a3117bfb8b1b2ffea614eb3`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a07e8dbc83b379142ab0610272789c07e7f137ebce010d7583561127873864f`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.5 MB (2535009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7759132941903777b7330a16aab22d0a1f1cec0454f6f147101486703c3ff`  
		Last Modified: Thu, 23 Jul 2020 07:43:46 GMT  
		Size: 60.9 MB (60877903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ef7df94104fcf347bbbe2c87b1b27db67b72b15808224c5a0eeff915e8f58`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; arm variant v5

```console
$ docker pull redmine@sha256:5cab9624d246de64a25b5a0643c3699eb7298d83bd724717a6cd5921361f84a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195786178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0551077dcdc64cb5d9d10adb8de7d142ff251ed6eee57cf390321418fdaf65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:13:17 GMT
ADD file:1a4c984d1bdb683e240e8bbdfeae45b146e1f8003444ce04a84096e58a437853 in / 
# Tue, 04 Aug 2020 03:13:27 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 13:32:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 13:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 13:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 13:40:38 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 13:40:39 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 13:40:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 13:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 13:44:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 13:44:15 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 22:28:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 22:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:36:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:36:54 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 22:36:57 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 22:36:57 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 22:37:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 22:37:08 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 22:37:08 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 22:37:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 22:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:42:52 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 22:42:53 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 22:42:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 22:42:57 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 22:42:59 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4eb4ac68461c572fdc826bae247c43484a232f91f165666714ce0f5f052b0bab`  
		Last Modified: Tue, 04 Aug 2020 03:34:09 GMT  
		Size: 24.8 MB (24836059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57be01b3add2b56b4059f291cb69f93d4ac64b65e2feab72dabebf63b1dfbfa`  
		Last Modified: Tue, 04 Aug 2020 14:08:05 GMT  
		Size: 10.3 MB (10327198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ea47e08f1c51e38e7a7cf0b08773f35502d2f4c74b9dc92a213c6d4541343`  
		Last Modified: Tue, 04 Aug 2020 14:08:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db84625521961fb028a86f0a5fc28c425020900a53caad2fca6d1a76f01383`  
		Last Modified: Tue, 04 Aug 2020 14:08:39 GMT  
		Size: 20.7 MB (20713715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2617e28f0f21cfb8e35961c52cf3ffd4057ad02f2775f22a457bf035795d62`  
		Last Modified: Tue, 04 Aug 2020 14:08:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3273f22201ce403089695a6076cc590163dc2f2a8434267db3056fffc5cd8`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745d6281cbab021152a30a4f6a353de13a21afb89552dcf2160257231622db63`  
		Last Modified: Tue, 04 Aug 2020 22:44:32 GMT  
		Size: 76.1 MB (76068284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1b9f5c3a4ffac38d0a36f0812063989e9e3cde1d4e82e6994c21a4b96ea08a`  
		Last Modified: Tue, 04 Aug 2020 22:44:08 GMT  
		Size: 1.3 MB (1314455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a371ca736eba3549aa02c7e837ab49104b1afc4b44cbbc06250d484378261c`  
		Last Modified: Tue, 04 Aug 2020 22:44:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e127a12494320c40b94686198f6d2eb3b05f99e7e38654fa0a2b966a5c78ed`  
		Last Modified: Tue, 04 Aug 2020 22:44:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa316b9187303a8bc9ec9b043776265c0b65caeb7e939e2355e7a22d0b33784`  
		Last Modified: Tue, 04 Aug 2020 22:44:07 GMT  
		Size: 2.5 MB (2535497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac12512db30c830589b2a42d0b2d891495b0e11c51835408ab1974187f000538`  
		Last Modified: Tue, 04 Aug 2020 22:44:21 GMT  
		Size: 60.0 MB (59986475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafdc3e57183a2612dace8a7ae7c7a8eb4be9776ed1d71c32d5a84bec84ddff4`  
		Last Modified: Tue, 04 Aug 2020 22:44:05 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c59c4cc19a61c10649637e26f61a8930a50af6703484fc03ddf11368fad0c1c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189134427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69a4639534cf392cb46605575073f17323ccc5f1e6da0dcae6cd5b3e849d4d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:43:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 19:06:31 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 19:06:32 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 19:06:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 19:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 19:10:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 19:11:04 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:33:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:40:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:40:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:40:44 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:40:47 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:40:51 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:41:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:41:11 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 07:41:13 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 07:41:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:46:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:46:07 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:46:09 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:46:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:46:13 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:46:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa146162a26aa547ba444d6ad8434a4fa88762f3a7d212b9931a93da93c0955`  
		Last Modified: Wed, 22 Jul 2020 19:44:54 GMT  
		Size: 9.8 MB (9847867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bbbb42b38aacfb77615f8d32c153836f2560cd16be8f9784f4bf30b3255e72`  
		Last Modified: Wed, 22 Jul 2020 19:44:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f040a4b29b55a0fbe2a9df84e9c2f36295a842b928b5db4a80edb5fa27b679`  
		Last Modified: Wed, 22 Jul 2020 19:45:26 GMT  
		Size: 20.6 MB (20622549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac7fe97b91d57334860f2cb01a6a29dd0964ebf470a743b88d7c6ca7e9dd4e`  
		Last Modified: Wed, 22 Jul 2020 19:45:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dadbfb2569aadf07131e4dd990e1ac49dfee4870545964b96d0e2a1bf5678a`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e0ea13aded1ce7251ad1a588080b1590f55b6ce64dc589ca9c0f043b482a54`  
		Last Modified: Thu, 23 Jul 2020 07:47:31 GMT  
		Size: 72.4 MB (72395846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e4eab866c4673d501aabad3ad5d808a07e590177f6ef10797db3596d7143ee`  
		Last Modified: Thu, 23 Jul 2020 07:47:07 GMT  
		Size: 1.3 MB (1304755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3573d010a5c2764f16d0e17c1e2b345fdcb92512cf18bb837efd994f00cf6621`  
		Last Modified: Thu, 23 Jul 2020 07:47:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1210f2f871d5bb715127e1b4ef42539822daff409a5a2063870a154abcf0d0f3`  
		Last Modified: Thu, 23 Jul 2020 07:47:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46939e830ced4e6374ad9bb78ae0044cf72b1a18ec4d5078575c58f5cd9a5542`  
		Last Modified: Thu, 23 Jul 2020 07:47:07 GMT  
		Size: 2.5 MB (2535507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e2898190dc09b95919da12934cbc47735cf56c9e7255195e7ba57597f0057`  
		Last Modified: Thu, 23 Jul 2020 07:47:20 GMT  
		Size: 59.7 MB (59717504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fe19b033c047b35a8c7fef3c66730c2b2445bd93fd17a7f2680d528a72a3b7`  
		Last Modified: Thu, 23 Jul 2020 07:47:05 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:8b9e592a28ab4b471f70df267d23bdb84ec8561a4649451922c5ab4319863944
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201860787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb23fe305418ef2cb1fc2e91109586c5c6927570cdd7dfa30afeca278213b5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:04:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:11:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:11:30 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:11:32 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:11:33 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:11:45 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 05:11:45 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 05:11:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:16:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:16:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:16:45 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:16:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:16:47 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:16:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c583882fde2e495b3f06f77cd3b3682d36bb918c14554cf30d2c7ee161dc9fb`  
		Last Modified: Thu, 23 Jul 2020 05:17:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c6e657542c66457d71773dc51409426a6c3c3e3850ff5ea5fef89042e89676`  
		Last Modified: Thu, 23 Jul 2020 05:18:05 GMT  
		Size: 78.8 MB (78833310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b83213c7c100025a12ed80c1565f69a2427307ceea82b70d3ab5e6b3ceeb90`  
		Last Modified: Thu, 23 Jul 2020 05:17:43 GMT  
		Size: 1.3 MB (1290975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59856d8208959620184862c438f36607210d3ef5de0bda3575b1147a0d1269e0`  
		Last Modified: Thu, 23 Jul 2020 05:17:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a884d9e13e73bc85d00ecac3427c840d0eae24533e954cfe0fc2c46ed0e1741`  
		Last Modified: Thu, 23 Jul 2020 05:17:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db6b4272221685420fbcf78ccdfdd7240f8015e60ee23878f31c867d10fdb67`  
		Last Modified: Thu, 23 Jul 2020 05:17:42 GMT  
		Size: 2.5 MB (2535505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0d724ceac8ee7ae4d7ebab40475ada35b3dfb0643174ccaf68480d680cbe88`  
		Last Modified: Thu, 23 Jul 2020 05:17:54 GMT  
		Size: 60.8 MB (60805476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2543b1f1de3ac2367b6c5f6d164bbec6e191316699163fbadf3a92e669e0032e`  
		Last Modified: Thu, 23 Jul 2020 05:17:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; 386

```console
$ docker pull redmine@sha256:fdee3f956688156989378eaa8b4bf13e458a853437e9dbfa0d93a69213077a70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211342322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deeed82a74dea306f67d0f77eadfc814c63d1ed4f3c8b733ce5b95937d24b1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:28:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 06:28:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 06:32:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 06:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 06:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:35:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 06:35:26 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 16:50:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 16:54:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 16:54:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:54:17 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 16:54:17 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 16:54:18 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 16:54:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 16:54:19 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 16:54:19 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 16:54:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 16:57:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:57:39 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 16:57:39 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 16:57:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 16:57:39 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 16:57:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a08c2806b9d07e191e456b4c558b5df63dd7de87f2e2b508835bbc5b74551e`  
		Last Modified: Tue, 04 Aug 2020 06:46:32 GMT  
		Size: 17.2 MB (17207416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0f87b9fa99941272a5d6e97848084b9a2e3fac033e8f975e9aed4c7687e4d`  
		Last Modified: Tue, 04 Aug 2020 06:46:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f9409304c0151340c860114b98b4afcdbf0fddf4925809919225625fa6291a`  
		Last Modified: Tue, 04 Aug 2020 06:46:43 GMT  
		Size: 20.9 MB (20884701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41b11b01ef197a4cbe56922dada1c4c9cd7d6d73775215b043968bb1092a22`  
		Last Modified: Tue, 04 Aug 2020 06:46:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97693b8301731105e8a914b2104d8e59ce5433f418755197a188bcde6af36196`  
		Last Modified: Tue, 04 Aug 2020 16:58:02 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16eed1d52f4ec29adbba4179d05ddea3800526a5fc29ec3be578faf08a445b6a`  
		Last Modified: Tue, 04 Aug 2020 16:59:05 GMT  
		Size: 81.6 MB (81645618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1a7365bcd00e37a029c64d5dc15bf6394735dc4cd6f5dadb52f1bbd631264`  
		Last Modified: Tue, 04 Aug 2020 16:58:42 GMT  
		Size: 1.3 MB (1326640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3334b58d340de03ebd03a1ec01f8254b20c119eed16b5761981c7de11d8da56`  
		Last Modified: Tue, 04 Aug 2020 16:58:40 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cab8f6188c58f0cd59c66a11d49f1f46041aa57f14a4ac3c795dad2ba9f0f9`  
		Last Modified: Tue, 04 Aug 2020 16:58:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54b2b38a5fd342820711e6273489b662db69cde3fc20725f6c327dcf46b8a8`  
		Last Modified: Tue, 04 Aug 2020 16:58:42 GMT  
		Size: 2.5 MB (2535010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a41b56de95f92c387c06cd44f0546383e4a2d2659098494a1a85eb9bf3a1cb`  
		Last Modified: Tue, 04 Aug 2020 16:58:56 GMT  
		Size: 60.0 MB (59988104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da96670b5aa1e721e7d20289c5cb5afcbac64a310102772d6fa98869eb804e7`  
		Last Modified: Tue, 04 Aug 2020 16:58:40 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; mips64le

```console
$ docker pull redmine@sha256:0993e946e6f2bdcc4a565fb80f1f947c29c7cd1578398f66e06919f392eb20ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201070243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60083ce34e151b154db3f0d5014a505d68bd01e06ba2a52fba3a5cf57bd9e1e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:23 GMT
ADD file:4164c71b841ba2c1f213c9fdc073ec3d4c7d79dadfcd9d771768750a3085d616 in / 
# Tue, 04 Aug 2020 06:42:24 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 14:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:28:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 14:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 14:36:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:36:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 14:36:43 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 23:36:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 23:45:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:45:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:45:42 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 23:45:42 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 23:45:43 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 23:45:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 23:45:45 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 23:45:45 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 23:45:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 23:53:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:53:24 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 23:53:24 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 23:53:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 23:53:25 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 23:53:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1333f76e75c0136aa2eb56b14271ef57d1f975f40fe2a56536d99b7c86c3aa29`  
		Last Modified: Tue, 04 Aug 2020 06:48:41 GMT  
		Size: 25.8 MB (25762724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db62010f6d33693e293c6f7e1f4a0ac8e25f991148111fd59ae56c62b6fb2952`  
		Last Modified: Tue, 04 Aug 2020 14:54:45 GMT  
		Size: 11.6 MB (11607928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4141050c0e58a8dddd238c62fd70b025302a9c8e8865cebf001dfebbb7c93b`  
		Last Modified: Tue, 04 Aug 2020 14:54:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d803382aa266318dfb2a52503c0eeb55d5fe9de18b3fbe835a9afbca7c0073d`  
		Last Modified: Tue, 04 Aug 2020 14:55:44 GMT  
		Size: 21.6 MB (21637848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3573e3ba846080432ddd673ddf9e5d802402ce3918ba7053368c28e01a963f5`  
		Last Modified: Tue, 04 Aug 2020 14:55:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcfb33ccf8f0380aa1d0b7f352cf240cf8df786b91de8d80306db3153f7d12`  
		Last Modified: Tue, 04 Aug 2020 23:53:39 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a736ce956d735192f44776c18fbfe2408e92a7b047e9b25bcc64b7ba217b49ce`  
		Last Modified: Tue, 04 Aug 2020 23:56:02 GMT  
		Size: 77.3 MB (77335293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5eef2396d0ce929b48256d919b7730bf5189e092a9cfd6a5c5782ce863934`  
		Last Modified: Tue, 04 Aug 2020 23:55:06 GMT  
		Size: 1.2 MB (1243184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeb51a2d1ea443d8d42fdd6bc6cf701e6e5d9aac1a97fdf3824dc2f5d295829`  
		Last Modified: Tue, 04 Aug 2020 23:55:02 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65858becdd1b7f8143f8ae95f83db55157e98ac9152f4e71bc41cc75bc5951ea`  
		Last Modified: Tue, 04 Aug 2020 23:55:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6351cf7a6080611e4938d3386c169026405e0c06ddf29990756549b80f7e87e4`  
		Last Modified: Tue, 04 Aug 2020 23:55:06 GMT  
		Size: 2.5 MB (2535008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd4cc34a24ea0bb6dcbba956ab8b0b7d6efbbd89c99d88883446587e7c6b3b5`  
		Last Modified: Tue, 04 Aug 2020 23:55:37 GMT  
		Size: 60.9 MB (60943848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c3790e650538acdb203f6ddd1753491eb41c35e07122986031fc2fdc262eb9`  
		Last Modified: Tue, 04 Aug 2020 23:55:02 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; ppc64le

```console
$ docker pull redmine@sha256:19967cb5483ba88ac9ee1a1ef8a55c57bfbca7dfb8f52bb96e1c309a13cac79c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217402766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0b1c442629c27db425c65556e85a0f51cf6cf173d233cfa6599077d43a3c20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:58:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:58:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 16:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 17:13:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 17:13:57 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 17:14:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 17:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 17:27:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 17:28:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 17:28:20 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:05:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:25:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:25:08 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:25:11 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:25:16 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:25:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:25:37 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 05:25:40 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 05:25:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:39:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:39:56 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:40:01 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:40:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:40:09 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:40:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4350e6f81db330ef296d21f9c43861e1d84a7979a7ab436c900ca40df5b93`  
		Last Modified: Wed, 22 Jul 2020 17:48:57 GMT  
		Size: 12.7 MB (12687936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b65160a4a21d5c38f87822df4ee82ca8a11f8b3785ea2120b3392402bf258a`  
		Last Modified: Wed, 22 Jul 2020 17:48:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6597f444d557392effc8b79dbf2c232ba5d941ebe724fa6249cf776cc29cf8`  
		Last Modified: Wed, 22 Jul 2020 17:49:48 GMT  
		Size: 22.0 MB (21970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a2a282b34bc40aad20adf0e7e9c38cad7b1a6855b7ec10705458b8d866a24`  
		Last Modified: Wed, 22 Jul 2020 17:49:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb3cce1a71287b14e02351ac19beaf109278c759f26ab033ea5d621320bba54`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e37e0be64b990addd251d0f9fdddeb87e20d72f84ebbba46ac3c28cbb2e216`  
		Last Modified: Thu, 23 Jul 2020 05:41:57 GMT  
		Size: 86.9 MB (86921419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2334ed06b483d738150dba7c7158c4f2854df32a02bc51464aec28882a179a29`  
		Last Modified: Thu, 23 Jul 2020 05:41:37 GMT  
		Size: 1.3 MB (1275771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062d640f81f37c02f7709d4b7f1c04d8f5820c40c0eb9575fa276afc5850242c`  
		Last Modified: Thu, 23 Jul 2020 05:41:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180999f24c7cccb8123968a2fa570afc8118c61a97950389328b9cd9a92656a`  
		Last Modified: Thu, 23 Jul 2020 05:41:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167975fda242188d5b0a0339cd2cf2187794dbc9eb6117ee2d134d696b41d07e`  
		Last Modified: Thu, 23 Jul 2020 05:41:31 GMT  
		Size: 2.5 MB (2535507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beed388de79a2865aa2236ac9d617bcde66eb81f6088fa45be01a46d97a338c4`  
		Last Modified: Thu, 23 Jul 2020 05:41:41 GMT  
		Size: 61.5 MB (61482589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb946c71e2ef4b1796f33380f85c1ea907e76248fbafc042b41d1efb5764c32b`  
		Last Modified: Thu, 23 Jul 2020 05:41:31 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.7` - linux; s390x

```console
$ docker pull redmine@sha256:a7d1d37430b4ab8bae6c6f3852e734208beeb4d2b9e3583f4a96f26d9d118426
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201288284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0fb07952267e3d0f167632ad977484cfc3afbc1e2ab4184c5e58dda9fd0ece`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:26:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 05:26:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 05:38:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 05:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:38:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 05:38:37 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 11:06:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 11:09:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:10:00 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 11:10:00 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 11:10:00 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 11:10:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 11:10:01 GMT
ENV REDMINE_VERSION=4.0.7
# Tue, 04 Aug 2020 11:10:01 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Tue, 04 Aug 2020 11:10:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 11:12:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:12:31 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 11:12:31 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 11:12:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 11:12:32 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 11:12:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e211a076d7bec7a39d1bc35ccd2ecfb97ecad9d15942b454d420c015aec78`  
		Last Modified: Tue, 04 Aug 2020 05:43:18 GMT  
		Size: 10.8 MB (10796400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea16a6f63db965daa21205a21bc3d56b39bc5415cb4fc0fbd4adc06bf68dbf`  
		Last Modified: Tue, 04 Aug 2020 05:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652803a9a3f37b5c0eb597d3cb545de4faeb3c8a0777c699a3b469318679edfc`  
		Last Modified: Tue, 04 Aug 2020 05:43:40 GMT  
		Size: 21.6 MB (21597298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661376aa0be2fb0f0f21b27678f8b46875aae059d564c4315df9156902b3fc58`  
		Last Modified: Tue, 04 Aug 2020 05:43:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9663cc42a0bb2db620a9f95bf2eac90ab8bb99edc3270b24130730ac855079`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07fbc7f0b2c4d4775f04fc7905722382aae9f503f30f6030e2eed8d85270293`  
		Last Modified: Tue, 04 Aug 2020 11:13:36 GMT  
		Size: 78.0 MB (77994752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bfb4ff00ef224f9003e27cbcb18cb2ceb68336c296173733770fb7292751d`  
		Last Modified: Tue, 04 Aug 2020 11:13:24 GMT  
		Size: 1.3 MB (1341792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632ad4b8a18acf543f13be6e341751e47b2d7c00bd3211efcff163ab6151bf7f`  
		Last Modified: Tue, 04 Aug 2020 11:13:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41c99ae0ddfbca193f8a35aebe77c61875b120da82d79bd9a3e11f70bad1c0`  
		Last Modified: Tue, 04 Aug 2020 11:13:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af22ef0a88d31b5c3e9b3084ddb80193cd77fccbe7b028d1f2a97d56eee1ee0`  
		Last Modified: Tue, 04 Aug 2020 11:13:23 GMT  
		Size: 2.5 MB (2535500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daa9f5c6767131d8df43ee05ad7c4cd4d4520b3a87200644902578c66c6291d`  
		Last Modified: Tue, 04 Aug 2020 11:13:29 GMT  
		Size: 61.3 MB (61310395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c182e03ed6ba8c148b60999836d2c27ef64d919853de976bb7bb250e0ca6dfe1`  
		Last Modified: Tue, 04 Aug 2020 11:13:23 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.7-alpine`

```console
$ docker pull redmine@sha256:ad7382f05ccf37ce1612e65b6a480211ab7d82e421cf40b8882d4158fb2142ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0.7-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:5ab5b25a7f6cd570c5dfe652fab11c71b2005262a5e5e84c3606c79a4e3a4b5b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172913667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201e41566cd75f7407ac15b8c4141bd86192131e9aa378924e24a484be64a7ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:01:32 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 13:01:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:31:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:58:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 22:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 22:02:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 22:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 22:02:57 GMT
CMD ["irb"]
# Sat, 27 Jun 2020 00:25:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 27 Jun 2020 00:31:21 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Sat, 27 Jun 2020 00:31:22 GMT
ENV RAILS_ENV=production
# Sat, 27 Jun 2020 00:31:22 GMT
WORKDIR /usr/src/redmine
# Sat, 27 Jun 2020 00:31:22 GMT
ENV HOME=/home/redmine
# Sat, 27 Jun 2020 00:31:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 27 Jun 2020 00:31:23 GMT
ENV REDMINE_VERSION=4.0.7
# Sat, 27 Jun 2020 00:31:23 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Sat, 27 Jun 2020 00:31:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 27 Jun 2020 00:33:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 27 Jun 2020 00:33:04 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 27 Jun 2020 00:33:04 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 27 Jun 2020 00:33:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jun 2020 00:33:05 GMT
EXPOSE 3000
# Sat, 27 Jun 2020 00:33:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ae8202b42d1c70c3a7f65680eabc1c562a29227549b9a1b33dc03943b20d2`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 1.1 MB (1131841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21786fe7c0d7561a5b89ca15d8a1c3e4ea673820cd79f1308bdfd8eb3cb7142`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb235115f8edc3a10cc9c312b6e1abb565211c93fa76ab48d17268515854e8be`  
		Last Modified: Fri, 26 Jun 2020 22:32:52 GMT  
		Size: 22.0 MB (22034884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c29a4c064b384d769d0155220d34ae1d2fddf90c92c2da398542082e780530`  
		Last Modified: Fri, 26 Jun 2020 22:32:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c476068e888bb1f351101b749200705a002008950a4e439b52a7b4c7d918fcb`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14876154f43c2933de788e3f4d1c5d8f032f1e67d81fe9950b35b0c036bc95b`  
		Last Modified: Sat, 27 Jun 2020 00:35:12 GMT  
		Size: 84.3 MB (84335465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7eef6551123b1102419f8867186a7430e1f29913c500ef5efa543f27818974`  
		Last Modified: Sat, 27 Jun 2020 00:34:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68ed76f4a7e483ddf6d602bfbd15c28c63ff1e062dbb401fc2e4523c79d8636`  
		Last Modified: Sat, 27 Jun 2020 00:34:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351e11b4834cabb36d0909293bb99b488be2f141b52752722f2c21bd34b33fb0`  
		Last Modified: Sat, 27 Jun 2020 00:34:54 GMT  
		Size: 2.5 MB (2536756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba48b7acabab37ea58cc7aaf5b2a2144576b846cab0b0b0be5ff157e55c024a`  
		Last Modified: Sat, 27 Jun 2020 00:35:01 GMT  
		Size: 60.1 MB (60057562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89734c2ad326a224a21a217c3bbbdf11b8d44e364c2998f9db5aa683adf41d63`  
		Last Modified: Sat, 27 Jun 2020 00:34:53 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.7-passenger`

```console
$ docker pull redmine@sha256:c0816ddd78ddc60f4679c38354cfbd1a8ec09bdc6cc75c8ab4e339ac11acbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0.7-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:9b444f6430c3464e81743ee7c947291250c6dc7f477eb4991b12004299736bb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230936707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e83056924c03b97bd450b2845414f43bb51e92690493790991903679e5fb5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:39:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:56 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:39:56 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:39:56 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:39:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 07:40:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:42:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:42:15 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:42:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:42:16 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:42:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 23 Jul 2020 07:42:26 GMT
ENV PASSENGER_VERSION=6.0.6
# Thu, 23 Jul 2020 07:42:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:42:44 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 23 Jul 2020 07:42:44 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 23 Jul 2020 07:42:44 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8421586d2cf63ecabb151095d53b7cc8a0d95a541b637313934d75701073d8e8`  
		Last Modified: Thu, 23 Jul 2020 07:43:53 GMT  
		Size: 80.2 MB (80200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1929ed7d3aeaa2c591151007973952a2665927e96155eac2493213095926d28b`  
		Last Modified: Thu, 23 Jul 2020 07:43:38 GMT  
		Size: 1.4 MB (1355992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f456cc6dd350a548741d36e834080e66862d12b35417e17cc6902bb2bad3065a`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f00e083cd2f3e056a2eca08b9c178cf998b0037a3117bfb8b1b2ffea614eb3`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a07e8dbc83b379142ab0610272789c07e7f137ebce010d7583561127873864f`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.5 MB (2535009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7759132941903777b7330a16aab22d0a1f1cec0454f6f147101486703c3ff`  
		Last Modified: Thu, 23 Jul 2020 07:43:46 GMT  
		Size: 60.9 MB (60877903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ef7df94104fcf347bbbe2c87b1b27db67b72b15808224c5a0eeff915e8f58`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845a90efb5943da4a834bb9b93082fe54966327656c0c03cd375227043ee53e6`  
		Last Modified: Thu, 23 Jul 2020 07:44:01 GMT  
		Size: 20.0 MB (19954366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105202ba3e0ab7ce0e1b3d1a58f683b1476ad10add1285bdfe9f0bdafaabee`  
		Last Modified: Thu, 23 Jul 2020 07:44:00 GMT  
		Size: 4.9 MB (4920447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-alpine`

```console
$ docker pull redmine@sha256:ad7382f05ccf37ce1612e65b6a480211ab7d82e421cf40b8882d4158fb2142ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:5ab5b25a7f6cd570c5dfe652fab11c71b2005262a5e5e84c3606c79a4e3a4b5b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172913667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201e41566cd75f7407ac15b8c4141bd86192131e9aa378924e24a484be64a7ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:01:32 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 13:01:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:31:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:58:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 22:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 22:02:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 22:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 22:02:57 GMT
CMD ["irb"]
# Sat, 27 Jun 2020 00:25:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 27 Jun 2020 00:31:21 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Sat, 27 Jun 2020 00:31:22 GMT
ENV RAILS_ENV=production
# Sat, 27 Jun 2020 00:31:22 GMT
WORKDIR /usr/src/redmine
# Sat, 27 Jun 2020 00:31:22 GMT
ENV HOME=/home/redmine
# Sat, 27 Jun 2020 00:31:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 27 Jun 2020 00:31:23 GMT
ENV REDMINE_VERSION=4.0.7
# Sat, 27 Jun 2020 00:31:23 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Sat, 27 Jun 2020 00:31:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 27 Jun 2020 00:33:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 27 Jun 2020 00:33:04 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 27 Jun 2020 00:33:04 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 27 Jun 2020 00:33:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jun 2020 00:33:05 GMT
EXPOSE 3000
# Sat, 27 Jun 2020 00:33:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ae8202b42d1c70c3a7f65680eabc1c562a29227549b9a1b33dc03943b20d2`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 1.1 MB (1131841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21786fe7c0d7561a5b89ca15d8a1c3e4ea673820cd79f1308bdfd8eb3cb7142`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb235115f8edc3a10cc9c312b6e1abb565211c93fa76ab48d17268515854e8be`  
		Last Modified: Fri, 26 Jun 2020 22:32:52 GMT  
		Size: 22.0 MB (22034884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c29a4c064b384d769d0155220d34ae1d2fddf90c92c2da398542082e780530`  
		Last Modified: Fri, 26 Jun 2020 22:32:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c476068e888bb1f351101b749200705a002008950a4e439b52a7b4c7d918fcb`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14876154f43c2933de788e3f4d1c5d8f032f1e67d81fe9950b35b0c036bc95b`  
		Last Modified: Sat, 27 Jun 2020 00:35:12 GMT  
		Size: 84.3 MB (84335465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7eef6551123b1102419f8867186a7430e1f29913c500ef5efa543f27818974`  
		Last Modified: Sat, 27 Jun 2020 00:34:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68ed76f4a7e483ddf6d602bfbd15c28c63ff1e062dbb401fc2e4523c79d8636`  
		Last Modified: Sat, 27 Jun 2020 00:34:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351e11b4834cabb36d0909293bb99b488be2f141b52752722f2c21bd34b33fb0`  
		Last Modified: Sat, 27 Jun 2020 00:34:54 GMT  
		Size: 2.5 MB (2536756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba48b7acabab37ea58cc7aaf5b2a2144576b846cab0b0b0be5ff157e55c024a`  
		Last Modified: Sat, 27 Jun 2020 00:35:01 GMT  
		Size: 60.1 MB (60057562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89734c2ad326a224a21a217c3bbbdf11b8d44e364c2998f9db5aa683adf41d63`  
		Last Modified: Sat, 27 Jun 2020 00:34:53 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-passenger`

```console
$ docker pull redmine@sha256:c0816ddd78ddc60f4679c38354cfbd1a8ec09bdc6cc75c8ab4e339ac11acbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:9b444f6430c3464e81743ee7c947291250c6dc7f477eb4991b12004299736bb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230936707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e83056924c03b97bd450b2845414f43bb51e92690493790991903679e5fb5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:39:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:56 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:39:56 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:39:56 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:39:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_VERSION=4.0.7
# Thu, 23 Jul 2020 07:39:57 GMT
ENV REDMINE_DOWNLOAD_MD5=baad690fdccd7f0282d53beb0ee2c47b
# Thu, 23 Jul 2020 07:40:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:42:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:42:15 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:42:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:42:16 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:42:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 23 Jul 2020 07:42:26 GMT
ENV PASSENGER_VERSION=6.0.6
# Thu, 23 Jul 2020 07:42:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:42:44 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 23 Jul 2020 07:42:44 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 23 Jul 2020 07:42:44 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8421586d2cf63ecabb151095d53b7cc8a0d95a541b637313934d75701073d8e8`  
		Last Modified: Thu, 23 Jul 2020 07:43:53 GMT  
		Size: 80.2 MB (80200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1929ed7d3aeaa2c591151007973952a2665927e96155eac2493213095926d28b`  
		Last Modified: Thu, 23 Jul 2020 07:43:38 GMT  
		Size: 1.4 MB (1355992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f456cc6dd350a548741d36e834080e66862d12b35417e17cc6902bb2bad3065a`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f00e083cd2f3e056a2eca08b9c178cf998b0037a3117bfb8b1b2ffea614eb3`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a07e8dbc83b379142ab0610272789c07e7f137ebce010d7583561127873864f`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.5 MB (2535009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7759132941903777b7330a16aab22d0a1f1cec0454f6f147101486703c3ff`  
		Last Modified: Thu, 23 Jul 2020 07:43:46 GMT  
		Size: 60.9 MB (60877903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ef7df94104fcf347bbbe2c87b1b27db67b72b15808224c5a0eeff915e8f58`  
		Last Modified: Thu, 23 Jul 2020 07:43:37 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845a90efb5943da4a834bb9b93082fe54966327656c0c03cd375227043ee53e6`  
		Last Modified: Thu, 23 Jul 2020 07:44:01 GMT  
		Size: 20.0 MB (19954366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105202ba3e0ab7ce0e1b3d1a58f683b1476ad10add1285bdfe9f0bdafaabee`  
		Last Modified: Thu, 23 Jul 2020 07:44:00 GMT  
		Size: 4.9 MB (4920447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1`

```console
$ docker pull redmine@sha256:d6f9a8543f565f71ca837800f6ebafdc419c4df9c4ade1f51ce0e39df93e5e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.1` - linux; amd64

```console
$ docker pull redmine@sha256:833e5d78c9753f2b2c13b4c69afe1cd149c5afaad67001d8a83a37b9245bc32f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216171855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809721a71330eac8df210b42075a82e9cc9dfbb2e7ff9b62c4facf44d4cecee0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2be89e251f2053dc73cf9a2bbfa3f4440486ec355fa6de5c71f570c3ed6e267c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204977614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea62738d5d1a33ebe7ecaac9ab95e1fa793b4293c4098ee771fccc0b52f68991`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:13:17 GMT
ADD file:1a4c984d1bdb683e240e8bbdfeae45b146e1f8003444ce04a84096e58a437853 in / 
# Tue, 04 Aug 2020 03:13:27 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 13:32:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 13:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 13:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 13:40:38 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 13:40:39 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 13:40:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 13:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 13:44:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 13:44:15 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 22:28:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 22:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:30:43 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 22:30:45 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 22:30:47 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 22:30:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 22:30:51 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 22:30:52 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 22:31:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 22:34:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:34:45 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 22:34:47 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 22:34:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 22:34:49 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 22:34:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4eb4ac68461c572fdc826bae247c43484a232f91f165666714ce0f5f052b0bab`  
		Last Modified: Tue, 04 Aug 2020 03:34:09 GMT  
		Size: 24.8 MB (24836059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57be01b3add2b56b4059f291cb69f93d4ac64b65e2feab72dabebf63b1dfbfa`  
		Last Modified: Tue, 04 Aug 2020 14:08:05 GMT  
		Size: 10.3 MB (10327198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ea47e08f1c51e38e7a7cf0b08773f35502d2f4c74b9dc92a213c6d4541343`  
		Last Modified: Tue, 04 Aug 2020 14:08:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db84625521961fb028a86f0a5fc28c425020900a53caad2fca6d1a76f01383`  
		Last Modified: Tue, 04 Aug 2020 14:08:39 GMT  
		Size: 20.7 MB (20713715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2617e28f0f21cfb8e35961c52cf3ffd4057ad02f2775f22a457bf035795d62`  
		Last Modified: Tue, 04 Aug 2020 14:08:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3273f22201ce403089695a6076cc590163dc2f2a8434267db3056fffc5cd8`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb2d746dedbf4eb6c0fc7b8cf24ddc2291b3c7e92cf9d177226d1162573e8b6`  
		Last Modified: Tue, 04 Aug 2020 22:43:53 GMT  
		Size: 88.7 MB (88696480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d31fb7f91b58955306a850427973eaf680db8961db69aca0c49b58c3abfac9`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.3 MB (1325699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0d2951fa1bcd46b4f5a6b6c7574d21153f4e1d81b95265569ac66c6aa1284b`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5875546d04cd4f74fb7987868f5e1e4849ee12c61736ea5018bb44a2a04049f0`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c2e8c98f73334e09c60b17bd68b19148fd7c0b3c01da9363710d5272f8f5c`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 2.7 MB (2739772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50816df5b9254ba96779634d05859aa7a60048dbb25d4b86dfcbdbfc1fde9e1`  
		Last Modified: Tue, 04 Aug 2020 22:43:34 GMT  
		Size: 56.3 MB (56334194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d81598a7a8cb7bfbc3e2a8d2a32e18cc7c29917fc0243026863d62a7524d`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v7

```console
$ docker pull redmine@sha256:355010891af82a27986c317860885449235e7e8d4af628ad31776a97e80b9e33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198630194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4331019b9e688ec87d1a2308c17c8f53091e0e4b085da9bedad20dc8ae238459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:43:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 19:06:31 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 19:06:32 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 19:06:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 19:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 19:10:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 19:11:04 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:33:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:34:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:34:48 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:34:49 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:34:51 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:35:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:35:01 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:35:03 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:35:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:31 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:41 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa146162a26aa547ba444d6ad8434a4fa88762f3a7d212b9931a93da93c0955`  
		Last Modified: Wed, 22 Jul 2020 19:44:54 GMT  
		Size: 9.8 MB (9847867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bbbb42b38aacfb77615f8d32c153836f2560cd16be8f9784f4bf30b3255e72`  
		Last Modified: Wed, 22 Jul 2020 19:44:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f040a4b29b55a0fbe2a9df84e9c2f36295a842b928b5db4a80edb5fa27b679`  
		Last Modified: Wed, 22 Jul 2020 19:45:26 GMT  
		Size: 20.6 MB (20622549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac7fe97b91d57334860f2cb01a6a29dd0964ebf470a743b88d7c6ca7e9dd4e`  
		Last Modified: Wed, 22 Jul 2020 19:45:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dadbfb2569aadf07131e4dd990e1ac49dfee4870545964b96d0e2a1bf5678a`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a449e1e40e99de1865735d2b279524408ea1351b8aa81990c736a782b2d4210`  
		Last Modified: Thu, 23 Jul 2020 07:46:56 GMT  
		Size: 84.7 MB (84733406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02264d74f8329975abccb71909a780753b498745c9ef75b979b9529502517e9`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.3 MB (1318462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca995ec3116e6ec1195a7325e0afc9e27fb189205a4d53354ac67960ed6f838c`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ac9b3e86c9a29035edf6253f0e3df0f051c408d77c156aa6494bcb7e0e676`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c7d4aab33d80e1b177cda6b60bb5f14dc8cb2d4300fed0343206c09794fa1`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 2.7 MB (2739760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfaceadd0e490522496ccb840e68c615f0c85962e979e12a7c225344503a22c`  
		Last Modified: Thu, 23 Jul 2020 07:46:40 GMT  
		Size: 56.7 MB (56657751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112d06851090b1ca1a75df2f0d09941ee63aaf2d2b969917b7c7f8175b4f8e01`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:c9f53b0d76ea524b605ff634f7209510fcc5d894df294941146f75e0335785d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211920019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e59d16f477d6c6a2074c97fe39006d6f853ed9c6eb64165a8d3d790b01464c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:04:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:06:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:06:24 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:06:25 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:06:26 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:06:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:06:28 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:06:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:09:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:09:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:09:48 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:09:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:09:50 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:09:50 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c583882fde2e495b3f06f77cd3b3682d36bb918c14554cf30d2c7ee161dc9fb`  
		Last Modified: Thu, 23 Jul 2020 05:17:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c4fba8eefa2b46a7263602929c34e267291ef9ca03717b53c9d1f048e4b56b`  
		Last Modified: Thu, 23 Jul 2020 05:17:32 GMT  
		Size: 91.7 MB (91696457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef07d6943d1c1b05f15ae85eca86998f7750f1c35e60b76fd22d341dc35c4a2`  
		Last Modified: Thu, 23 Jul 2020 05:17:07 GMT  
		Size: 1.3 MB (1303026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab54a1ad31cd224479ac9699ee04c4c1b0f6fc19e1b92f1e6200f1efc4078e5`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc39b484b0cffbe92301f619ded4e936d75c51f602db9df2d6a50ca98f93048`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f8474208e65fa214067edf1ba7e78ee6eb8f8014f2fd712e43f1bd61f37f11`  
		Last Modified: Thu, 23 Jul 2020 05:17:05 GMT  
		Size: 2.7 MB (2739764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cd6feb09fd25ec692cfeabdcc33b943450bc7b7023d1a486512b473061da3f`  
		Last Modified: Thu, 23 Jul 2020 05:17:17 GMT  
		Size: 57.8 MB (57785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb362d000fbcd290102b537fadd3d40b9c9381049b8f6e3e4155e68bdecebd`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; 386

```console
$ docker pull redmine@sha256:f2178363f078c2aa301ca51ef99ca2eadf97d3ba954df8fad98d6728d951ca62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221021322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22cbfb1abd0184f1c39ac5d3bf265c48d40d098127ac12ae6317c47a94627a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:28:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 06:28:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 06:32:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 06:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 06:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:35:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 06:35:26 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 16:50:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 16:50:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 16:51:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:51:04 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 16:51:04 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 16:51:04 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 16:51:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 16:51:05 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 16:51:06 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 16:51:09 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 16:53:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:53:29 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 16:53:29 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 16:53:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 16:53:30 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 16:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a08c2806b9d07e191e456b4c558b5df63dd7de87f2e2b508835bbc5b74551e`  
		Last Modified: Tue, 04 Aug 2020 06:46:32 GMT  
		Size: 17.2 MB (17207416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0f87b9fa99941272a5d6e97848084b9a2e3fac033e8f975e9aed4c7687e4d`  
		Last Modified: Tue, 04 Aug 2020 06:46:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f9409304c0151340c860114b98b4afcdbf0fddf4925809919225625fa6291a`  
		Last Modified: Tue, 04 Aug 2020 06:46:43 GMT  
		Size: 20.9 MB (20884701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41b11b01ef197a4cbe56922dada1c4c9cd7d6d73775215b043968bb1092a22`  
		Last Modified: Tue, 04 Aug 2020 06:46:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97693b8301731105e8a914b2104d8e59ce5433f418755197a188bcde6af36196`  
		Last Modified: Tue, 04 Aug 2020 16:58:02 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc245d7e0ea3f04564d84cf94b177be72a6b039a756fa3cb0907352f8f1a3422`  
		Last Modified: Tue, 04 Aug 2020 16:58:34 GMT  
		Size: 94.7 MB (94730198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88ee83d219cc1dbd9f7aa390edc15772cfdc5ceca4829b80d0530e10bcd9c6`  
		Last Modified: Tue, 04 Aug 2020 16:58:04 GMT  
		Size: 1.3 MB (1337849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db434591aaf6b2104717ecc1073aaff73538a54505a7db0a5f1358dfb8818f00`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d155abeeea3550d021c1769122bb4c305d1b81366c73d13a7660111ab335ff`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c1770c1229ca1b059c643cdf10a02545db6192f0092f8a984569b91eece17b`  
		Last Modified: Tue, 04 Aug 2020 16:58:03 GMT  
		Size: 2.7 MB (2739481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925451a24c00a15b578826e1ef3d8102dd2400ec2f77334952157e4d81ac05c8`  
		Last Modified: Tue, 04 Aug 2020 16:58:16 GMT  
		Size: 56.4 MB (56366844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e593ee226ab0b438ea9e0653a6a8106aa816dd64eed2d2670c2464f9f00462`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; mips64le

```console
$ docker pull redmine@sha256:cf580d908948f74b725b71af887645cfedb9fc589b3b32dc0708e56c92679dbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210450731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d78379974db691acab79ddb59be559e9424fefa68da382ccdf36edab08da9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:23 GMT
ADD file:4164c71b841ba2c1f213c9fdc073ec3d4c7d79dadfcd9d771768750a3085d616 in / 
# Tue, 04 Aug 2020 06:42:24 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 14:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:28:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 14:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 14:36:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:36:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 14:36:43 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 23:36:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 23:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:38:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:38:16 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 23:38:16 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 23:38:16 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 23:38:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 23:38:18 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 23:38:19 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 23:38:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 23:44:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:44:05 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 23:44:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 23:44:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 23:44:06 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 23:44:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1333f76e75c0136aa2eb56b14271ef57d1f975f40fe2a56536d99b7c86c3aa29`  
		Last Modified: Tue, 04 Aug 2020 06:48:41 GMT  
		Size: 25.8 MB (25762724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db62010f6d33693e293c6f7e1f4a0ac8e25f991148111fd59ae56c62b6fb2952`  
		Last Modified: Tue, 04 Aug 2020 14:54:45 GMT  
		Size: 11.6 MB (11607928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4141050c0e58a8dddd238c62fd70b025302a9c8e8865cebf001dfebbb7c93b`  
		Last Modified: Tue, 04 Aug 2020 14:54:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d803382aa266318dfb2a52503c0eeb55d5fe9de18b3fbe835a9afbca7c0073d`  
		Last Modified: Tue, 04 Aug 2020 14:55:44 GMT  
		Size: 21.6 MB (21637848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3573e3ba846080432ddd673ddf9e5d802402ce3918ba7053368c28e01a963f5`  
		Last Modified: Tue, 04 Aug 2020 14:55:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcfb33ccf8f0380aa1d0b7f352cf240cf8df786b91de8d80306db3153f7d12`  
		Last Modified: Tue, 04 Aug 2020 23:53:39 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dad1bd5ce73a7a970dc0d953cc42236f7ffa5b528a6af0eaa234586c3335bb`  
		Last Modified: Tue, 04 Aug 2020 23:54:46 GMT  
		Size: 90.1 MB (90079123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43391042277f010d07116bcaf9e1aa4c325dc2c50dee6011fa8e7e1085e7edd9`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 1.3 MB (1256601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99da4257b265b0c9fa53948454fc184f3e851a1f1ac4b5aa67a678c66d265860`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf806cf56575cea106d5e3ebc5168d3f3cf7c52431d69fc1739e4f7c69e72f3`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a385f169e3df2bd1f65afc062b46112b75ee76f0fd39fdbb067ca743fc884a`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 2.7 MB (2739480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913c98a27840a8b69cdf53041383bce1fe2d778f91983aed82a9ed39d37061fc`  
		Last Modified: Tue, 04 Aug 2020 23:54:08 GMT  
		Size: 57.4 MB (57362619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b052041f3ba260c6a5fd48151a512025362178e7dc882f6959b65597602d8`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; ppc64le

```console
$ docker pull redmine@sha256:470af361a42a77d0c7ef84e405dcc86d264fd7ce9e7767bac317d396848f30ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227983214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619b68c811c421da7ad2e9e7b5c67de5f6a2a08b7dc0514ea681f2e65fac321`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:58:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:58:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 16:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 17:13:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 17:13:57 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 17:14:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 17:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 17:27:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 17:28:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 17:28:20 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:05:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:11:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:12:03 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:12:11 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:12:13 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:12:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:12:31 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:12:38 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:12:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:18:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:18:53 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:18:56 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:19:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:19:10 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:19:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4350e6f81db330ef296d21f9c43861e1d84a7979a7ab436c900ca40df5b93`  
		Last Modified: Wed, 22 Jul 2020 17:48:57 GMT  
		Size: 12.7 MB (12687936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b65160a4a21d5c38f87822df4ee82ca8a11f8b3785ea2120b3392402bf258a`  
		Last Modified: Wed, 22 Jul 2020 17:48:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6597f444d557392effc8b79dbf2c232ba5d941ebe724fa6249cf776cc29cf8`  
		Last Modified: Wed, 22 Jul 2020 17:49:48 GMT  
		Size: 22.0 MB (21970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a2a282b34bc40aad20adf0e7e9c38cad7b1a6855b7ec10705458b8d866a24`  
		Last Modified: Wed, 22 Jul 2020 17:49:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb3cce1a71287b14e02351ac19beaf109278c759f26ab033ea5d621320bba54`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f236001c13bbc805a1e4713ad6c5ed0e476464eacdfd44ba608a418c1877d007`  
		Last Modified: Thu, 23 Jul 2020 05:41:12 GMT  
		Size: 100.3 MB (100344362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aead886d739bd3bc027292813e19b942521fd83e2b87b84d7ffc57cf359fd04d`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.3 MB (1290010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf6afd72f85c187c4e3cd56894c0bd2fc5342847b64e204b8380d74572930c`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c518dbadfc9a2b2040e19141f943668ca44272fa3522b735d8d40966dcc238bc`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b813ca710fb3e9cf25dea3c2473a35f4165a8c4d1cb4e3c1209547b4b1da26ce`  
		Last Modified: Thu, 23 Jul 2020 05:40:47 GMT  
		Size: 2.7 MB (2739767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927698c2c46c1e2009a7d99151cb2489579f4c2d2c6b43be64618a6915bff86`  
		Last Modified: Thu, 23 Jul 2020 05:40:55 GMT  
		Size: 58.4 MB (58421593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b0e2e590831a782eae54596172a684f302529c2726b8e70b6136621a7dcc83`  
		Last Modified: Thu, 23 Jul 2020 05:40:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; s390x

```console
$ docker pull redmine@sha256:9cacc436f5e29968b595f56a05fb9a85d8cf599ad03ff9e513f249d68d9e2b1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210720601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84be3ab4689f85e4e730235b2d5605c6aed59471c02fa85ef7d8370f46a85d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:26:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 05:26:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 05:38:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 05:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:38:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 05:38:37 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 11:06:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 11:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:07:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:07:31 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 11:07:31 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 11:07:32 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 11:07:33 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 11:07:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 11:09:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:09:19 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 11:09:19 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 11:09:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 11:09:19 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 11:09:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e211a076d7bec7a39d1bc35ccd2ecfb97ecad9d15942b454d420c015aec78`  
		Last Modified: Tue, 04 Aug 2020 05:43:18 GMT  
		Size: 10.8 MB (10796400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea16a6f63db965daa21205a21bc3d56b39bc5415cb4fc0fbd4adc06bf68dbf`  
		Last Modified: Tue, 04 Aug 2020 05:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652803a9a3f37b5c0eb597d3cb545de4faeb3c8a0777c699a3b469318679edfc`  
		Last Modified: Tue, 04 Aug 2020 05:43:40 GMT  
		Size: 21.6 MB (21597298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661376aa0be2fb0f0f21b27678f8b46875aae059d564c4315df9156902b3fc58`  
		Last Modified: Tue, 04 Aug 2020 05:43:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9663cc42a0bb2db620a9f95bf2eac90ab8bb99edc3270b24130730ac855079`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4fee1c0fdf6aa4e3bdf1ad574569cc4b91918ecccf3121781b6222a536c493`  
		Last Modified: Tue, 04 Aug 2020 11:13:14 GMT  
		Size: 90.9 MB (90854185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a738a595cfdd936a270ac3a839188391d9a832eb23a682df205b380edef952`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.4 MB (1355115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4ded94c32cc1762576dc5d1895c8ff2a61981a4b18f844ab529a5bc3f11a60`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4fc727b1933c0c8e1ec90802948f0caa3068693f5edc86e07fc249ba40c9c7`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9d70d6ba3b29079423c01dae21a4f44b5de6687dc28b84909413ddf4de164f`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.7 MB (2739769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5248a897bfb0f149c6c341f108ecccd52d07ffd97ed1aeea3bf0872bf4654f`  
		Last Modified: Tue, 04 Aug 2020 11:13:05 GMT  
		Size: 57.7 MB (57665687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaad00d5183f9814d6f3c76d671245eff35857f941e9587960a79408ae0116e`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.1`

```console
$ docker pull redmine@sha256:d6f9a8543f565f71ca837800f6ebafdc419c4df9c4ade1f51ce0e39df93e5e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.1.1` - linux; amd64

```console
$ docker pull redmine@sha256:833e5d78c9753f2b2c13b4c69afe1cd149c5afaad67001d8a83a37b9245bc32f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216171855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809721a71330eac8df210b42075a82e9cc9dfbb2e7ff9b62c4facf44d4cecee0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2be89e251f2053dc73cf9a2bbfa3f4440486ec355fa6de5c71f570c3ed6e267c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204977614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea62738d5d1a33ebe7ecaac9ab95e1fa793b4293c4098ee771fccc0b52f68991`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:13:17 GMT
ADD file:1a4c984d1bdb683e240e8bbdfeae45b146e1f8003444ce04a84096e58a437853 in / 
# Tue, 04 Aug 2020 03:13:27 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 13:32:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 13:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 13:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 13:40:38 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 13:40:39 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 13:40:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 13:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 13:44:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 13:44:15 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 22:28:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 22:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:30:43 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 22:30:45 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 22:30:47 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 22:30:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 22:30:51 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 22:30:52 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 22:31:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 22:34:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:34:45 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 22:34:47 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 22:34:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 22:34:49 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 22:34:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4eb4ac68461c572fdc826bae247c43484a232f91f165666714ce0f5f052b0bab`  
		Last Modified: Tue, 04 Aug 2020 03:34:09 GMT  
		Size: 24.8 MB (24836059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57be01b3add2b56b4059f291cb69f93d4ac64b65e2feab72dabebf63b1dfbfa`  
		Last Modified: Tue, 04 Aug 2020 14:08:05 GMT  
		Size: 10.3 MB (10327198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ea47e08f1c51e38e7a7cf0b08773f35502d2f4c74b9dc92a213c6d4541343`  
		Last Modified: Tue, 04 Aug 2020 14:08:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db84625521961fb028a86f0a5fc28c425020900a53caad2fca6d1a76f01383`  
		Last Modified: Tue, 04 Aug 2020 14:08:39 GMT  
		Size: 20.7 MB (20713715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2617e28f0f21cfb8e35961c52cf3ffd4057ad02f2775f22a457bf035795d62`  
		Last Modified: Tue, 04 Aug 2020 14:08:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3273f22201ce403089695a6076cc590163dc2f2a8434267db3056fffc5cd8`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb2d746dedbf4eb6c0fc7b8cf24ddc2291b3c7e92cf9d177226d1162573e8b6`  
		Last Modified: Tue, 04 Aug 2020 22:43:53 GMT  
		Size: 88.7 MB (88696480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d31fb7f91b58955306a850427973eaf680db8961db69aca0c49b58c3abfac9`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.3 MB (1325699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0d2951fa1bcd46b4f5a6b6c7574d21153f4e1d81b95265569ac66c6aa1284b`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5875546d04cd4f74fb7987868f5e1e4849ee12c61736ea5018bb44a2a04049f0`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c2e8c98f73334e09c60b17bd68b19148fd7c0b3c01da9363710d5272f8f5c`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 2.7 MB (2739772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50816df5b9254ba96779634d05859aa7a60048dbb25d4b86dfcbdbfc1fde9e1`  
		Last Modified: Tue, 04 Aug 2020 22:43:34 GMT  
		Size: 56.3 MB (56334194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d81598a7a8cb7bfbc3e2a8d2a32e18cc7c29917fc0243026863d62a7524d`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; arm variant v7

```console
$ docker pull redmine@sha256:355010891af82a27986c317860885449235e7e8d4af628ad31776a97e80b9e33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198630194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4331019b9e688ec87d1a2308c17c8f53091e0e4b085da9bedad20dc8ae238459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:43:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 19:06:31 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 19:06:32 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 19:06:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 19:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 19:10:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 19:11:04 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:33:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:34:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:34:48 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:34:49 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:34:51 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:35:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:35:01 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:35:03 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:35:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:31 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:41 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa146162a26aa547ba444d6ad8434a4fa88762f3a7d212b9931a93da93c0955`  
		Last Modified: Wed, 22 Jul 2020 19:44:54 GMT  
		Size: 9.8 MB (9847867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bbbb42b38aacfb77615f8d32c153836f2560cd16be8f9784f4bf30b3255e72`  
		Last Modified: Wed, 22 Jul 2020 19:44:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f040a4b29b55a0fbe2a9df84e9c2f36295a842b928b5db4a80edb5fa27b679`  
		Last Modified: Wed, 22 Jul 2020 19:45:26 GMT  
		Size: 20.6 MB (20622549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac7fe97b91d57334860f2cb01a6a29dd0964ebf470a743b88d7c6ca7e9dd4e`  
		Last Modified: Wed, 22 Jul 2020 19:45:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dadbfb2569aadf07131e4dd990e1ac49dfee4870545964b96d0e2a1bf5678a`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a449e1e40e99de1865735d2b279524408ea1351b8aa81990c736a782b2d4210`  
		Last Modified: Thu, 23 Jul 2020 07:46:56 GMT  
		Size: 84.7 MB (84733406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02264d74f8329975abccb71909a780753b498745c9ef75b979b9529502517e9`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.3 MB (1318462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca995ec3116e6ec1195a7325e0afc9e27fb189205a4d53354ac67960ed6f838c`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ac9b3e86c9a29035edf6253f0e3df0f051c408d77c156aa6494bcb7e0e676`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c7d4aab33d80e1b177cda6b60bb5f14dc8cb2d4300fed0343206c09794fa1`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 2.7 MB (2739760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfaceadd0e490522496ccb840e68c615f0c85962e979e12a7c225344503a22c`  
		Last Modified: Thu, 23 Jul 2020 07:46:40 GMT  
		Size: 56.7 MB (56657751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112d06851090b1ca1a75df2f0d09941ee63aaf2d2b969917b7c7f8175b4f8e01`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:c9f53b0d76ea524b605ff634f7209510fcc5d894df294941146f75e0335785d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211920019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e59d16f477d6c6a2074c97fe39006d6f853ed9c6eb64165a8d3d790b01464c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:04:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:06:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:06:24 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:06:25 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:06:26 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:06:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:06:28 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:06:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:09:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:09:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:09:48 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:09:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:09:50 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:09:50 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c583882fde2e495b3f06f77cd3b3682d36bb918c14554cf30d2c7ee161dc9fb`  
		Last Modified: Thu, 23 Jul 2020 05:17:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c4fba8eefa2b46a7263602929c34e267291ef9ca03717b53c9d1f048e4b56b`  
		Last Modified: Thu, 23 Jul 2020 05:17:32 GMT  
		Size: 91.7 MB (91696457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef07d6943d1c1b05f15ae85eca86998f7750f1c35e60b76fd22d341dc35c4a2`  
		Last Modified: Thu, 23 Jul 2020 05:17:07 GMT  
		Size: 1.3 MB (1303026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab54a1ad31cd224479ac9699ee04c4c1b0f6fc19e1b92f1e6200f1efc4078e5`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc39b484b0cffbe92301f619ded4e936d75c51f602db9df2d6a50ca98f93048`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f8474208e65fa214067edf1ba7e78ee6eb8f8014f2fd712e43f1bd61f37f11`  
		Last Modified: Thu, 23 Jul 2020 05:17:05 GMT  
		Size: 2.7 MB (2739764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cd6feb09fd25ec692cfeabdcc33b943450bc7b7023d1a486512b473061da3f`  
		Last Modified: Thu, 23 Jul 2020 05:17:17 GMT  
		Size: 57.8 MB (57785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb362d000fbcd290102b537fadd3d40b9c9381049b8f6e3e4155e68bdecebd`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; 386

```console
$ docker pull redmine@sha256:f2178363f078c2aa301ca51ef99ca2eadf97d3ba954df8fad98d6728d951ca62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221021322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22cbfb1abd0184f1c39ac5d3bf265c48d40d098127ac12ae6317c47a94627a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:28:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 06:28:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 06:32:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 06:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 06:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:35:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 06:35:26 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 16:50:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 16:50:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 16:51:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:51:04 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 16:51:04 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 16:51:04 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 16:51:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 16:51:05 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 16:51:06 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 16:51:09 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 16:53:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:53:29 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 16:53:29 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 16:53:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 16:53:30 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 16:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a08c2806b9d07e191e456b4c558b5df63dd7de87f2e2b508835bbc5b74551e`  
		Last Modified: Tue, 04 Aug 2020 06:46:32 GMT  
		Size: 17.2 MB (17207416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0f87b9fa99941272a5d6e97848084b9a2e3fac033e8f975e9aed4c7687e4d`  
		Last Modified: Tue, 04 Aug 2020 06:46:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f9409304c0151340c860114b98b4afcdbf0fddf4925809919225625fa6291a`  
		Last Modified: Tue, 04 Aug 2020 06:46:43 GMT  
		Size: 20.9 MB (20884701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41b11b01ef197a4cbe56922dada1c4c9cd7d6d73775215b043968bb1092a22`  
		Last Modified: Tue, 04 Aug 2020 06:46:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97693b8301731105e8a914b2104d8e59ce5433f418755197a188bcde6af36196`  
		Last Modified: Tue, 04 Aug 2020 16:58:02 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc245d7e0ea3f04564d84cf94b177be72a6b039a756fa3cb0907352f8f1a3422`  
		Last Modified: Tue, 04 Aug 2020 16:58:34 GMT  
		Size: 94.7 MB (94730198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88ee83d219cc1dbd9f7aa390edc15772cfdc5ceca4829b80d0530e10bcd9c6`  
		Last Modified: Tue, 04 Aug 2020 16:58:04 GMT  
		Size: 1.3 MB (1337849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db434591aaf6b2104717ecc1073aaff73538a54505a7db0a5f1358dfb8818f00`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d155abeeea3550d021c1769122bb4c305d1b81366c73d13a7660111ab335ff`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c1770c1229ca1b059c643cdf10a02545db6192f0092f8a984569b91eece17b`  
		Last Modified: Tue, 04 Aug 2020 16:58:03 GMT  
		Size: 2.7 MB (2739481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925451a24c00a15b578826e1ef3d8102dd2400ec2f77334952157e4d81ac05c8`  
		Last Modified: Tue, 04 Aug 2020 16:58:16 GMT  
		Size: 56.4 MB (56366844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e593ee226ab0b438ea9e0653a6a8106aa816dd64eed2d2670c2464f9f00462`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; mips64le

```console
$ docker pull redmine@sha256:cf580d908948f74b725b71af887645cfedb9fc589b3b32dc0708e56c92679dbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210450731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d78379974db691acab79ddb59be559e9424fefa68da382ccdf36edab08da9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:23 GMT
ADD file:4164c71b841ba2c1f213c9fdc073ec3d4c7d79dadfcd9d771768750a3085d616 in / 
# Tue, 04 Aug 2020 06:42:24 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 14:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:28:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 14:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 14:36:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:36:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 14:36:43 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 23:36:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 23:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:38:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:38:16 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 23:38:16 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 23:38:16 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 23:38:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 23:38:18 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 23:38:19 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 23:38:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 23:44:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:44:05 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 23:44:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 23:44:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 23:44:06 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 23:44:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1333f76e75c0136aa2eb56b14271ef57d1f975f40fe2a56536d99b7c86c3aa29`  
		Last Modified: Tue, 04 Aug 2020 06:48:41 GMT  
		Size: 25.8 MB (25762724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db62010f6d33693e293c6f7e1f4a0ac8e25f991148111fd59ae56c62b6fb2952`  
		Last Modified: Tue, 04 Aug 2020 14:54:45 GMT  
		Size: 11.6 MB (11607928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4141050c0e58a8dddd238c62fd70b025302a9c8e8865cebf001dfebbb7c93b`  
		Last Modified: Tue, 04 Aug 2020 14:54:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d803382aa266318dfb2a52503c0eeb55d5fe9de18b3fbe835a9afbca7c0073d`  
		Last Modified: Tue, 04 Aug 2020 14:55:44 GMT  
		Size: 21.6 MB (21637848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3573e3ba846080432ddd673ddf9e5d802402ce3918ba7053368c28e01a963f5`  
		Last Modified: Tue, 04 Aug 2020 14:55:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcfb33ccf8f0380aa1d0b7f352cf240cf8df786b91de8d80306db3153f7d12`  
		Last Modified: Tue, 04 Aug 2020 23:53:39 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dad1bd5ce73a7a970dc0d953cc42236f7ffa5b528a6af0eaa234586c3335bb`  
		Last Modified: Tue, 04 Aug 2020 23:54:46 GMT  
		Size: 90.1 MB (90079123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43391042277f010d07116bcaf9e1aa4c325dc2c50dee6011fa8e7e1085e7edd9`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 1.3 MB (1256601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99da4257b265b0c9fa53948454fc184f3e851a1f1ac4b5aa67a678c66d265860`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf806cf56575cea106d5e3ebc5168d3f3cf7c52431d69fc1739e4f7c69e72f3`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a385f169e3df2bd1f65afc062b46112b75ee76f0fd39fdbb067ca743fc884a`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 2.7 MB (2739480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913c98a27840a8b69cdf53041383bce1fe2d778f91983aed82a9ed39d37061fc`  
		Last Modified: Tue, 04 Aug 2020 23:54:08 GMT  
		Size: 57.4 MB (57362619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b052041f3ba260c6a5fd48151a512025362178e7dc882f6959b65597602d8`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; ppc64le

```console
$ docker pull redmine@sha256:470af361a42a77d0c7ef84e405dcc86d264fd7ce9e7767bac317d396848f30ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227983214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619b68c811c421da7ad2e9e7b5c67de5f6a2a08b7dc0514ea681f2e65fac321`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:58:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:58:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 16:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 17:13:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 17:13:57 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 17:14:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 17:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 17:27:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 17:28:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 17:28:20 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:05:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:11:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:12:03 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:12:11 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:12:13 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:12:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:12:31 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:12:38 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:12:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:18:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:18:53 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:18:56 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:19:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:19:10 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:19:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4350e6f81db330ef296d21f9c43861e1d84a7979a7ab436c900ca40df5b93`  
		Last Modified: Wed, 22 Jul 2020 17:48:57 GMT  
		Size: 12.7 MB (12687936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b65160a4a21d5c38f87822df4ee82ca8a11f8b3785ea2120b3392402bf258a`  
		Last Modified: Wed, 22 Jul 2020 17:48:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6597f444d557392effc8b79dbf2c232ba5d941ebe724fa6249cf776cc29cf8`  
		Last Modified: Wed, 22 Jul 2020 17:49:48 GMT  
		Size: 22.0 MB (21970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a2a282b34bc40aad20adf0e7e9c38cad7b1a6855b7ec10705458b8d866a24`  
		Last Modified: Wed, 22 Jul 2020 17:49:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb3cce1a71287b14e02351ac19beaf109278c759f26ab033ea5d621320bba54`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f236001c13bbc805a1e4713ad6c5ed0e476464eacdfd44ba608a418c1877d007`  
		Last Modified: Thu, 23 Jul 2020 05:41:12 GMT  
		Size: 100.3 MB (100344362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aead886d739bd3bc027292813e19b942521fd83e2b87b84d7ffc57cf359fd04d`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.3 MB (1290010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf6afd72f85c187c4e3cd56894c0bd2fc5342847b64e204b8380d74572930c`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c518dbadfc9a2b2040e19141f943668ca44272fa3522b735d8d40966dcc238bc`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b813ca710fb3e9cf25dea3c2473a35f4165a8c4d1cb4e3c1209547b4b1da26ce`  
		Last Modified: Thu, 23 Jul 2020 05:40:47 GMT  
		Size: 2.7 MB (2739767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927698c2c46c1e2009a7d99151cb2489579f4c2d2c6b43be64618a6915bff86`  
		Last Modified: Thu, 23 Jul 2020 05:40:55 GMT  
		Size: 58.4 MB (58421593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b0e2e590831a782eae54596172a684f302529c2726b8e70b6136621a7dcc83`  
		Last Modified: Thu, 23 Jul 2020 05:40:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.1` - linux; s390x

```console
$ docker pull redmine@sha256:9cacc436f5e29968b595f56a05fb9a85d8cf599ad03ff9e513f249d68d9e2b1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210720601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84be3ab4689f85e4e730235b2d5605c6aed59471c02fa85ef7d8370f46a85d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:26:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 05:26:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 05:38:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 05:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:38:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 05:38:37 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 11:06:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 11:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:07:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:07:31 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 11:07:31 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 11:07:32 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 11:07:33 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 11:07:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 11:09:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:09:19 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 11:09:19 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 11:09:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 11:09:19 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 11:09:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e211a076d7bec7a39d1bc35ccd2ecfb97ecad9d15942b454d420c015aec78`  
		Last Modified: Tue, 04 Aug 2020 05:43:18 GMT  
		Size: 10.8 MB (10796400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea16a6f63db965daa21205a21bc3d56b39bc5415cb4fc0fbd4adc06bf68dbf`  
		Last Modified: Tue, 04 Aug 2020 05:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652803a9a3f37b5c0eb597d3cb545de4faeb3c8a0777c699a3b469318679edfc`  
		Last Modified: Tue, 04 Aug 2020 05:43:40 GMT  
		Size: 21.6 MB (21597298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661376aa0be2fb0f0f21b27678f8b46875aae059d564c4315df9156902b3fc58`  
		Last Modified: Tue, 04 Aug 2020 05:43:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9663cc42a0bb2db620a9f95bf2eac90ab8bb99edc3270b24130730ac855079`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4fee1c0fdf6aa4e3bdf1ad574569cc4b91918ecccf3121781b6222a536c493`  
		Last Modified: Tue, 04 Aug 2020 11:13:14 GMT  
		Size: 90.9 MB (90854185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a738a595cfdd936a270ac3a839188391d9a832eb23a682df205b380edef952`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.4 MB (1355115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4ded94c32cc1762576dc5d1895c8ff2a61981a4b18f844ab529a5bc3f11a60`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4fc727b1933c0c8e1ec90802948f0caa3068693f5edc86e07fc249ba40c9c7`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9d70d6ba3b29079423c01dae21a4f44b5de6687dc28b84909413ddf4de164f`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.7 MB (2739769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5248a897bfb0f149c6c341f108ecccd52d07ffd97ed1aeea3bf0872bf4654f`  
		Last Modified: Tue, 04 Aug 2020 11:13:05 GMT  
		Size: 57.7 MB (57665687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaad00d5183f9814d6f3c76d671245eff35857f941e9587960a79408ae0116e`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.1-alpine`

```console
$ docker pull redmine@sha256:deb3e5905b57732069ca7a8101139f4d03539698d15761948fb68e7fcccfbbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1.1-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:78fd8d9d940ba992e2a33b657fda2b4cf88782b14790107bf768d45177dd6cc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171497540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a1414db38346739e8aea9ca4c9b429ab68eab03a71c8bd6410e5a295fd4981`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:01:32 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 13:01:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:31:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:58:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 22:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 22:02:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 22:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 22:02:57 GMT
CMD ["irb"]
# Sat, 27 Jun 2020 00:25:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 27 Jun 2020 00:25:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 27 Jun 2020 00:25:27 GMT
ENV RAILS_ENV=production
# Sat, 27 Jun 2020 00:25:27 GMT
WORKDIR /usr/src/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
ENV HOME=/home/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_VERSION=4.1.1
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Sat, 27 Jun 2020 00:25:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 27 Jun 2020 00:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 27 Jun 2020 00:27:17 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 27 Jun 2020 00:27:17 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 27 Jun 2020 00:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jun 2020 00:27:17 GMT
EXPOSE 3000
# Sat, 27 Jun 2020 00:27:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ae8202b42d1c70c3a7f65680eabc1c562a29227549b9a1b33dc03943b20d2`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 1.1 MB (1131841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21786fe7c0d7561a5b89ca15d8a1c3e4ea673820cd79f1308bdfd8eb3cb7142`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb235115f8edc3a10cc9c312b6e1abb565211c93fa76ab48d17268515854e8be`  
		Last Modified: Fri, 26 Jun 2020 22:32:52 GMT  
		Size: 22.0 MB (22034884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c29a4c064b384d769d0155220d34ae1d2fddf90c92c2da398542082e780530`  
		Last Modified: Fri, 26 Jun 2020 22:32:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c476068e888bb1f351101b749200705a002008950a4e439b52a7b4c7d918fcb`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45862f5b557674a750247e6b190c60394e0b39aabe07d9b9aaf93d692898e2c4`  
		Last Modified: Sat, 27 Jun 2020 00:34:16 GMT  
		Size: 86.4 MB (86363568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6acc4528111e9b0ffe75dbb915d2acab87480fde026496ddce3b83fe8ec1de`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1784ebb8ec3fd8526b0fa4bf0b54698e1bcd7b576e438d69593d8e83a58b0827`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa2fd8dfdffc038300d0b8bc6adc0e71e6f0f79c354fdec413049bb35475c9`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 2.7 MB (2740358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4d7861d6f4c034c489f4c7b07e64beba357d0cdaa623e10207d11da6156b4`  
		Last Modified: Sat, 27 Jun 2020 00:34:08 GMT  
		Size: 56.4 MB (56409729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376d9ce0b49da4e05452216d93a5a6d8637962c939c8499a7f8b70649283474`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.1-passenger`

```console
$ docker pull redmine@sha256:03d9af0c2ca87b7616d4840215153c2e197e90ffb688aaa7d4256a9522bbb6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1.1-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:b6ac2a73471e47140756a2b13d76ecdaa35f73d2d7cae6c9bb3190752ee5c891
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241044548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd51b224bd422e274789598472d83448ec2875abfe851e232ad9c8797baecc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 23 Jul 2020 07:38:57 GMT
ENV PASSENGER_VERSION=6.0.6
# Thu, 23 Jul 2020 07:39:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:15 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 23 Jul 2020 07:39:15 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 23 Jul 2020 07:39:15 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99902f714402485f8d8b64277c5572d9a10ada60e58740726e237d8b48187d19`  
		Last Modified: Thu, 23 Jul 2020 07:43:31 GMT  
		Size: 20.0 MB (19952240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d01d908740d1afae692b875052e99be2e6fc83c460822b7b8109614ada45a5`  
		Last Modified: Thu, 23 Jul 2020 07:43:29 GMT  
		Size: 4.9 MB (4920453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-alpine`

```console
$ docker pull redmine@sha256:deb3e5905b57732069ca7a8101139f4d03539698d15761948fb68e7fcccfbbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:78fd8d9d940ba992e2a33b657fda2b4cf88782b14790107bf768d45177dd6cc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171497540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a1414db38346739e8aea9ca4c9b429ab68eab03a71c8bd6410e5a295fd4981`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:01:32 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 13:01:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:31:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:58:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 22:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 22:02:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 22:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 22:02:57 GMT
CMD ["irb"]
# Sat, 27 Jun 2020 00:25:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 27 Jun 2020 00:25:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 27 Jun 2020 00:25:27 GMT
ENV RAILS_ENV=production
# Sat, 27 Jun 2020 00:25:27 GMT
WORKDIR /usr/src/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
ENV HOME=/home/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_VERSION=4.1.1
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Sat, 27 Jun 2020 00:25:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 27 Jun 2020 00:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 27 Jun 2020 00:27:17 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 27 Jun 2020 00:27:17 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 27 Jun 2020 00:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jun 2020 00:27:17 GMT
EXPOSE 3000
# Sat, 27 Jun 2020 00:27:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ae8202b42d1c70c3a7f65680eabc1c562a29227549b9a1b33dc03943b20d2`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 1.1 MB (1131841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21786fe7c0d7561a5b89ca15d8a1c3e4ea673820cd79f1308bdfd8eb3cb7142`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb235115f8edc3a10cc9c312b6e1abb565211c93fa76ab48d17268515854e8be`  
		Last Modified: Fri, 26 Jun 2020 22:32:52 GMT  
		Size: 22.0 MB (22034884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c29a4c064b384d769d0155220d34ae1d2fddf90c92c2da398542082e780530`  
		Last Modified: Fri, 26 Jun 2020 22:32:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c476068e888bb1f351101b749200705a002008950a4e439b52a7b4c7d918fcb`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45862f5b557674a750247e6b190c60394e0b39aabe07d9b9aaf93d692898e2c4`  
		Last Modified: Sat, 27 Jun 2020 00:34:16 GMT  
		Size: 86.4 MB (86363568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6acc4528111e9b0ffe75dbb915d2acab87480fde026496ddce3b83fe8ec1de`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1784ebb8ec3fd8526b0fa4bf0b54698e1bcd7b576e438d69593d8e83a58b0827`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa2fd8dfdffc038300d0b8bc6adc0e71e6f0f79c354fdec413049bb35475c9`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 2.7 MB (2740358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4d7861d6f4c034c489f4c7b07e64beba357d0cdaa623e10207d11da6156b4`  
		Last Modified: Sat, 27 Jun 2020 00:34:08 GMT  
		Size: 56.4 MB (56409729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376d9ce0b49da4e05452216d93a5a6d8637962c939c8499a7f8b70649283474`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-passenger`

```console
$ docker pull redmine@sha256:03d9af0c2ca87b7616d4840215153c2e197e90ffb688aaa7d4256a9522bbb6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:b6ac2a73471e47140756a2b13d76ecdaa35f73d2d7cae6c9bb3190752ee5c891
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241044548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd51b224bd422e274789598472d83448ec2875abfe851e232ad9c8797baecc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 23 Jul 2020 07:38:57 GMT
ENV PASSENGER_VERSION=6.0.6
# Thu, 23 Jul 2020 07:39:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:15 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 23 Jul 2020 07:39:15 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 23 Jul 2020 07:39:15 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99902f714402485f8d8b64277c5572d9a10ada60e58740726e237d8b48187d19`  
		Last Modified: Thu, 23 Jul 2020 07:43:31 GMT  
		Size: 20.0 MB (19952240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d01d908740d1afae692b875052e99be2e6fc83c460822b7b8109614ada45a5`  
		Last Modified: Thu, 23 Jul 2020 07:43:29 GMT  
		Size: 4.9 MB (4920453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:deb3e5905b57732069ca7a8101139f4d03539698d15761948fb68e7fcccfbbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:78fd8d9d940ba992e2a33b657fda2b4cf88782b14790107bf768d45177dd6cc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171497540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a1414db38346739e8aea9ca4c9b429ab68eab03a71c8bd6410e5a295fd4981`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:01:32 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 13:01:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:31:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:58:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 22:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 22:02:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 22:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 22:02:57 GMT
CMD ["irb"]
# Sat, 27 Jun 2020 00:25:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 27 Jun 2020 00:25:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 27 Jun 2020 00:25:27 GMT
ENV RAILS_ENV=production
# Sat, 27 Jun 2020 00:25:27 GMT
WORKDIR /usr/src/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
ENV HOME=/home/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_VERSION=4.1.1
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Sat, 27 Jun 2020 00:25:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 27 Jun 2020 00:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 27 Jun 2020 00:27:17 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 27 Jun 2020 00:27:17 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 27 Jun 2020 00:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jun 2020 00:27:17 GMT
EXPOSE 3000
# Sat, 27 Jun 2020 00:27:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ae8202b42d1c70c3a7f65680eabc1c562a29227549b9a1b33dc03943b20d2`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 1.1 MB (1131841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21786fe7c0d7561a5b89ca15d8a1c3e4ea673820cd79f1308bdfd8eb3cb7142`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb235115f8edc3a10cc9c312b6e1abb565211c93fa76ab48d17268515854e8be`  
		Last Modified: Fri, 26 Jun 2020 22:32:52 GMT  
		Size: 22.0 MB (22034884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c29a4c064b384d769d0155220d34ae1d2fddf90c92c2da398542082e780530`  
		Last Modified: Fri, 26 Jun 2020 22:32:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c476068e888bb1f351101b749200705a002008950a4e439b52a7b4c7d918fcb`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45862f5b557674a750247e6b190c60394e0b39aabe07d9b9aaf93d692898e2c4`  
		Last Modified: Sat, 27 Jun 2020 00:34:16 GMT  
		Size: 86.4 MB (86363568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6acc4528111e9b0ffe75dbb915d2acab87480fde026496ddce3b83fe8ec1de`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1784ebb8ec3fd8526b0fa4bf0b54698e1bcd7b576e438d69593d8e83a58b0827`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa2fd8dfdffc038300d0b8bc6adc0e71e6f0f79c354fdec413049bb35475c9`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 2.7 MB (2740358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4d7861d6f4c034c489f4c7b07e64beba357d0cdaa623e10207d11da6156b4`  
		Last Modified: Sat, 27 Jun 2020 00:34:08 GMT  
		Size: 56.4 MB (56409729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376d9ce0b49da4e05452216d93a5a6d8637962c939c8499a7f8b70649283474`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:03d9af0c2ca87b7616d4840215153c2e197e90ffb688aaa7d4256a9522bbb6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:b6ac2a73471e47140756a2b13d76ecdaa35f73d2d7cae6c9bb3190752ee5c891
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241044548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd51b224bd422e274789598472d83448ec2875abfe851e232ad9c8797baecc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 23 Jul 2020 07:38:57 GMT
ENV PASSENGER_VERSION=6.0.6
# Thu, 23 Jul 2020 07:39:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:15 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 23 Jul 2020 07:39:15 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 23 Jul 2020 07:39:15 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99902f714402485f8d8b64277c5572d9a10ada60e58740726e237d8b48187d19`  
		Last Modified: Thu, 23 Jul 2020 07:43:31 GMT  
		Size: 20.0 MB (19952240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d01d908740d1afae692b875052e99be2e6fc83c460822b7b8109614ada45a5`  
		Last Modified: Thu, 23 Jul 2020 07:43:29 GMT  
		Size: 4.9 MB (4920453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:alpine`

```console
$ docker pull redmine@sha256:deb3e5905b57732069ca7a8101139f4d03539698d15761948fb68e7fcccfbbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:78fd8d9d940ba992e2a33b657fda2b4cf88782b14790107bf768d45177dd6cc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171497540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a1414db38346739e8aea9ca4c9b429ab68eab03a71c8bd6410e5a295fd4981`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:01:32 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 13:01:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:31:26 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:58:01 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:58:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 22:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 22:02:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 22:02:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 22:02:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 22:02:57 GMT
CMD ["irb"]
# Sat, 27 Jun 2020 00:25:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 27 Jun 2020 00:25:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 27 Jun 2020 00:25:27 GMT
ENV RAILS_ENV=production
# Sat, 27 Jun 2020 00:25:27 GMT
WORKDIR /usr/src/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
ENV HOME=/home/redmine
# Sat, 27 Jun 2020 00:25:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_VERSION=4.1.1
# Sat, 27 Jun 2020 00:25:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Sat, 27 Jun 2020 00:25:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 27 Jun 2020 00:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 27 Jun 2020 00:27:17 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 27 Jun 2020 00:27:17 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 27 Jun 2020 00:27:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jun 2020 00:27:17 GMT
EXPOSE 3000
# Sat, 27 Jun 2020 00:27:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ae8202b42d1c70c3a7f65680eabc1c562a29227549b9a1b33dc03943b20d2`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 1.1 MB (1131841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21786fe7c0d7561a5b89ca15d8a1c3e4ea673820cd79f1308bdfd8eb3cb7142`  
		Last Modified: Fri, 24 Apr 2020 13:21:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb235115f8edc3a10cc9c312b6e1abb565211c93fa76ab48d17268515854e8be`  
		Last Modified: Fri, 26 Jun 2020 22:32:52 GMT  
		Size: 22.0 MB (22034884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c29a4c064b384d769d0155220d34ae1d2fddf90c92c2da398542082e780530`  
		Last Modified: Fri, 26 Jun 2020 22:32:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c476068e888bb1f351101b749200705a002008950a4e439b52a7b4c7d918fcb`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45862f5b557674a750247e6b190c60394e0b39aabe07d9b9aaf93d692898e2c4`  
		Last Modified: Sat, 27 Jun 2020 00:34:16 GMT  
		Size: 86.4 MB (86363568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6acc4528111e9b0ffe75dbb915d2acab87480fde026496ddce3b83fe8ec1de`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1784ebb8ec3fd8526b0fa4bf0b54698e1bcd7b576e438d69593d8e83a58b0827`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa2fd8dfdffc038300d0b8bc6adc0e71e6f0f79c354fdec413049bb35475c9`  
		Last Modified: Sat, 27 Jun 2020 00:33:58 GMT  
		Size: 2.7 MB (2740358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4d7861d6f4c034c489f4c7b07e64beba357d0cdaa623e10207d11da6156b4`  
		Last Modified: Sat, 27 Jun 2020 00:34:08 GMT  
		Size: 56.4 MB (56409729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376d9ce0b49da4e05452216d93a5a6d8637962c939c8499a7f8b70649283474`  
		Last Modified: Sat, 27 Jun 2020 00:33:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:d6f9a8543f565f71ca837800f6ebafdc419c4df9c4ade1f51ce0e39df93e5e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:833e5d78c9753f2b2c13b4c69afe1cd149c5afaad67001d8a83a37b9245bc32f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216171855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809721a71330eac8df210b42075a82e9cc9dfbb2e7ff9b62c4facf44d4cecee0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2be89e251f2053dc73cf9a2bbfa3f4440486ec355fa6de5c71f570c3ed6e267c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204977614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea62738d5d1a33ebe7ecaac9ab95e1fa793b4293c4098ee771fccc0b52f68991`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:13:17 GMT
ADD file:1a4c984d1bdb683e240e8bbdfeae45b146e1f8003444ce04a84096e58a437853 in / 
# Tue, 04 Aug 2020 03:13:27 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 13:32:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 13:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 13:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 13:40:38 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 13:40:39 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 13:40:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 13:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 13:44:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 13:44:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 13:44:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 13:44:15 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 22:28:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 22:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 22:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:30:43 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 22:30:45 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 22:30:47 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 22:30:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 22:30:51 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 22:30:52 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 22:31:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 22:34:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 22:34:45 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 22:34:47 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 22:34:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 22:34:49 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 22:34:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4eb4ac68461c572fdc826bae247c43484a232f91f165666714ce0f5f052b0bab`  
		Last Modified: Tue, 04 Aug 2020 03:34:09 GMT  
		Size: 24.8 MB (24836059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57be01b3add2b56b4059f291cb69f93d4ac64b65e2feab72dabebf63b1dfbfa`  
		Last Modified: Tue, 04 Aug 2020 14:08:05 GMT  
		Size: 10.3 MB (10327198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ea47e08f1c51e38e7a7cf0b08773f35502d2f4c74b9dc92a213c6d4541343`  
		Last Modified: Tue, 04 Aug 2020 14:08:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db84625521961fb028a86f0a5fc28c425020900a53caad2fca6d1a76f01383`  
		Last Modified: Tue, 04 Aug 2020 14:08:39 GMT  
		Size: 20.7 MB (20713715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2617e28f0f21cfb8e35961c52cf3ffd4057ad02f2775f22a457bf035795d62`  
		Last Modified: Tue, 04 Aug 2020 14:08:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3273f22201ce403089695a6076cc590163dc2f2a8434267db3056fffc5cd8`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb2d746dedbf4eb6c0fc7b8cf24ddc2291b3c7e92cf9d177226d1162573e8b6`  
		Last Modified: Tue, 04 Aug 2020 22:43:53 GMT  
		Size: 88.7 MB (88696480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d31fb7f91b58955306a850427973eaf680db8961db69aca0c49b58c3abfac9`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 1.3 MB (1325699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0d2951fa1bcd46b4f5a6b6c7574d21153f4e1d81b95265569ac66c6aa1284b`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5875546d04cd4f74fb7987868f5e1e4849ee12c61736ea5018bb44a2a04049f0`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c2e8c98f73334e09c60b17bd68b19148fd7c0b3c01da9363710d5272f8f5c`  
		Last Modified: Tue, 04 Aug 2020 22:43:23 GMT  
		Size: 2.7 MB (2739772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50816df5b9254ba96779634d05859aa7a60048dbb25d4b86dfcbdbfc1fde9e1`  
		Last Modified: Tue, 04 Aug 2020 22:43:34 GMT  
		Size: 56.3 MB (56334194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d81598a7a8cb7bfbc3e2a8d2a32e18cc7c29917fc0243026863d62a7524d`  
		Last Modified: Tue, 04 Aug 2020 22:43:21 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:355010891af82a27986c317860885449235e7e8d4af628ad31776a97e80b9e33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198630194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4331019b9e688ec87d1a2308c17c8f53091e0e4b085da9bedad20dc8ae238459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:43:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 19:06:31 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 19:06:32 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 19:06:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 19:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 19:10:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 19:10:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 19:11:04 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:33:14 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:34:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:34:48 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:34:49 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:34:51 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:35:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:35:01 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:35:03 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:35:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:31 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:41 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa146162a26aa547ba444d6ad8434a4fa88762f3a7d212b9931a93da93c0955`  
		Last Modified: Wed, 22 Jul 2020 19:44:54 GMT  
		Size: 9.8 MB (9847867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bbbb42b38aacfb77615f8d32c153836f2560cd16be8f9784f4bf30b3255e72`  
		Last Modified: Wed, 22 Jul 2020 19:44:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f040a4b29b55a0fbe2a9df84e9c2f36295a842b928b5db4a80edb5fa27b679`  
		Last Modified: Wed, 22 Jul 2020 19:45:26 GMT  
		Size: 20.6 MB (20622549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac7fe97b91d57334860f2cb01a6a29dd0964ebf470a743b88d7c6ca7e9dd4e`  
		Last Modified: Wed, 22 Jul 2020 19:45:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dadbfb2569aadf07131e4dd990e1ac49dfee4870545964b96d0e2a1bf5678a`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a449e1e40e99de1865735d2b279524408ea1351b8aa81990c736a782b2d4210`  
		Last Modified: Thu, 23 Jul 2020 07:46:56 GMT  
		Size: 84.7 MB (84733406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02264d74f8329975abccb71909a780753b498745c9ef75b979b9529502517e9`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 1.3 MB (1318462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca995ec3116e6ec1195a7325e0afc9e27fb189205a4d53354ac67960ed6f838c`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ac9b3e86c9a29035edf6253f0e3df0f051c408d77c156aa6494bcb7e0e676`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c7d4aab33d80e1b177cda6b60bb5f14dc8cb2d4300fed0343206c09794fa1`  
		Last Modified: Thu, 23 Jul 2020 07:46:28 GMT  
		Size: 2.7 MB (2739760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfaceadd0e490522496ccb840e68c615f0c85962e979e12a7c225344503a22c`  
		Last Modified: Thu, 23 Jul 2020 07:46:40 GMT  
		Size: 56.7 MB (56657751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112d06851090b1ca1a75df2f0d09941ee63aaf2d2b969917b7c7f8175b4f8e01`  
		Last Modified: Thu, 23 Jul 2020 07:46:26 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:c9f53b0d76ea524b605ff634f7209510fcc5d894df294941146f75e0335785d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211920019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e59d16f477d6c6a2074c97fe39006d6f853ed9c6eb64165a8d3d790b01464c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:04:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:06:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:06:24 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:06:25 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:06:26 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:06:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:06:28 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:06:29 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:06:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:09:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:09:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:09:48 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:09:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:09:50 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:09:50 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c583882fde2e495b3f06f77cd3b3682d36bb918c14554cf30d2c7ee161dc9fb`  
		Last Modified: Thu, 23 Jul 2020 05:17:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c4fba8eefa2b46a7263602929c34e267291ef9ca03717b53c9d1f048e4b56b`  
		Last Modified: Thu, 23 Jul 2020 05:17:32 GMT  
		Size: 91.7 MB (91696457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef07d6943d1c1b05f15ae85eca86998f7750f1c35e60b76fd22d341dc35c4a2`  
		Last Modified: Thu, 23 Jul 2020 05:17:07 GMT  
		Size: 1.3 MB (1303026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab54a1ad31cd224479ac9699ee04c4c1b0f6fc19e1b92f1e6200f1efc4078e5`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc39b484b0cffbe92301f619ded4e936d75c51f602db9df2d6a50ca98f93048`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f8474208e65fa214067edf1ba7e78ee6eb8f8014f2fd712e43f1bd61f37f11`  
		Last Modified: Thu, 23 Jul 2020 05:17:05 GMT  
		Size: 2.7 MB (2739764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cd6feb09fd25ec692cfeabdcc33b943450bc7b7023d1a486512b473061da3f`  
		Last Modified: Thu, 23 Jul 2020 05:17:17 GMT  
		Size: 57.8 MB (57785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb362d000fbcd290102b537fadd3d40b9c9381049b8f6e3e4155e68bdecebd`  
		Last Modified: Thu, 23 Jul 2020 05:17:04 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:f2178363f078c2aa301ca51ef99ca2eadf97d3ba954df8fad98d6728d951ca62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221021322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22cbfb1abd0184f1c39ac5d3bf265c48d40d098127ac12ae6317c47a94627a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:28:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 06:28:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 06:32:19 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 06:32:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 06:35:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 06:35:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 06:35:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:35:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 06:35:26 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 16:50:21 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 16:50:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 16:51:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:51:04 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 16:51:04 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 16:51:04 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 16:51:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 16:51:05 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 16:51:06 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 16:51:09 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 16:53:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 16:53:29 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 16:53:29 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 16:53:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 16:53:30 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 16:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a08c2806b9d07e191e456b4c558b5df63dd7de87f2e2b508835bbc5b74551e`  
		Last Modified: Tue, 04 Aug 2020 06:46:32 GMT  
		Size: 17.2 MB (17207416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0f87b9fa99941272a5d6e97848084b9a2e3fac033e8f975e9aed4c7687e4d`  
		Last Modified: Tue, 04 Aug 2020 06:46:27 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f9409304c0151340c860114b98b4afcdbf0fddf4925809919225625fa6291a`  
		Last Modified: Tue, 04 Aug 2020 06:46:43 GMT  
		Size: 20.9 MB (20884701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41b11b01ef197a4cbe56922dada1c4c9cd7d6d73775215b043968bb1092a22`  
		Last Modified: Tue, 04 Aug 2020 06:46:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97693b8301731105e8a914b2104d8e59ce5433f418755197a188bcde6af36196`  
		Last Modified: Tue, 04 Aug 2020 16:58:02 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc245d7e0ea3f04564d84cf94b177be72a6b039a756fa3cb0907352f8f1a3422`  
		Last Modified: Tue, 04 Aug 2020 16:58:34 GMT  
		Size: 94.7 MB (94730198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88ee83d219cc1dbd9f7aa390edc15772cfdc5ceca4829b80d0530e10bcd9c6`  
		Last Modified: Tue, 04 Aug 2020 16:58:04 GMT  
		Size: 1.3 MB (1337849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db434591aaf6b2104717ecc1073aaff73538a54505a7db0a5f1358dfb8818f00`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d155abeeea3550d021c1769122bb4c305d1b81366c73d13a7660111ab335ff`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c1770c1229ca1b059c643cdf10a02545db6192f0092f8a984569b91eece17b`  
		Last Modified: Tue, 04 Aug 2020 16:58:03 GMT  
		Size: 2.7 MB (2739481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925451a24c00a15b578826e1ef3d8102dd2400ec2f77334952157e4d81ac05c8`  
		Last Modified: Tue, 04 Aug 2020 16:58:16 GMT  
		Size: 56.4 MB (56366844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e593ee226ab0b438ea9e0653a6a8106aa816dd64eed2d2670c2464f9f00462`  
		Last Modified: Tue, 04 Aug 2020 16:58:01 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; mips64le

```console
$ docker pull redmine@sha256:cf580d908948f74b725b71af887645cfedb9fc589b3b32dc0708e56c92679dbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210450731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d78379974db691acab79ddb59be559e9424fefa68da382ccdf36edab08da9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:23 GMT
ADD file:4164c71b841ba2c1f213c9fdc073ec3d4c7d79dadfcd9d771768750a3085d616 in / 
# Tue, 04 Aug 2020 06:42:24 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:10:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 14:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:28:09 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 14:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 14:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 14:36:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 14:36:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:36:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 14:36:43 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 23:36:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 23:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:38:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:38:16 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 23:38:16 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 23:38:16 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 23:38:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 23:38:18 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 23:38:19 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 23:38:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 23:44:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 23:44:05 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 23:44:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 23:44:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 23:44:06 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 23:44:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1333f76e75c0136aa2eb56b14271ef57d1f975f40fe2a56536d99b7c86c3aa29`  
		Last Modified: Tue, 04 Aug 2020 06:48:41 GMT  
		Size: 25.8 MB (25762724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db62010f6d33693e293c6f7e1f4a0ac8e25f991148111fd59ae56c62b6fb2952`  
		Last Modified: Tue, 04 Aug 2020 14:54:45 GMT  
		Size: 11.6 MB (11607928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4141050c0e58a8dddd238c62fd70b025302a9c8e8865cebf001dfebbb7c93b`  
		Last Modified: Tue, 04 Aug 2020 14:54:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d803382aa266318dfb2a52503c0eeb55d5fe9de18b3fbe835a9afbca7c0073d`  
		Last Modified: Tue, 04 Aug 2020 14:55:44 GMT  
		Size: 21.6 MB (21637848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3573e3ba846080432ddd673ddf9e5d802402ce3918ba7053368c28e01a963f5`  
		Last Modified: Tue, 04 Aug 2020 14:55:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcfb33ccf8f0380aa1d0b7f352cf240cf8df786b91de8d80306db3153f7d12`  
		Last Modified: Tue, 04 Aug 2020 23:53:39 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dad1bd5ce73a7a970dc0d953cc42236f7ffa5b528a6af0eaa234586c3335bb`  
		Last Modified: Tue, 04 Aug 2020 23:54:46 GMT  
		Size: 90.1 MB (90079123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43391042277f010d07116bcaf9e1aa4c325dc2c50dee6011fa8e7e1085e7edd9`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 1.3 MB (1256601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99da4257b265b0c9fa53948454fc184f3e851a1f1ac4b5aa67a678c66d265860`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf806cf56575cea106d5e3ebc5168d3f3cf7c52431d69fc1739e4f7c69e72f3`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a385f169e3df2bd1f65afc062b46112b75ee76f0fd39fdbb067ca743fc884a`  
		Last Modified: Tue, 04 Aug 2020 23:53:40 GMT  
		Size: 2.7 MB (2739480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913c98a27840a8b69cdf53041383bce1fe2d778f91983aed82a9ed39d37061fc`  
		Last Modified: Tue, 04 Aug 2020 23:54:08 GMT  
		Size: 57.4 MB (57362619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b052041f3ba260c6a5fd48151a512025362178e7dc882f6959b65597602d8`  
		Last Modified: Tue, 04 Aug 2020 23:53:36 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:470af361a42a77d0c7ef84e405dcc86d264fd7ce9e7767bac317d396848f30ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227983214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619b68c811c421da7ad2e9e7b5c67de5f6a2a08b7dc0514ea681f2e65fac321`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:58:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:58:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 16:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 17:13:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 17:13:57 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 17:14:02 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 17:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 17:27:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 17:27:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 17:28:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 17:28:20 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:05:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 05:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:11:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:12:03 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 05:12:11 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 05:12:13 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 05:12:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 05:12:31 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 05:12:38 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 05:12:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 05:18:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 05:18:53 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 05:18:56 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 05:19:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:19:10 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 05:19:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4350e6f81db330ef296d21f9c43861e1d84a7979a7ab436c900ca40df5b93`  
		Last Modified: Wed, 22 Jul 2020 17:48:57 GMT  
		Size: 12.7 MB (12687936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b65160a4a21d5c38f87822df4ee82ca8a11f8b3785ea2120b3392402bf258a`  
		Last Modified: Wed, 22 Jul 2020 17:48:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6597f444d557392effc8b79dbf2c232ba5d941ebe724fa6249cf776cc29cf8`  
		Last Modified: Wed, 22 Jul 2020 17:49:48 GMT  
		Size: 22.0 MB (21970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a2a282b34bc40aad20adf0e7e9c38cad7b1a6855b7ec10705458b8d866a24`  
		Last Modified: Wed, 22 Jul 2020 17:49:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb3cce1a71287b14e02351ac19beaf109278c759f26ab033ea5d621320bba54`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f236001c13bbc805a1e4713ad6c5ed0e476464eacdfd44ba608a418c1877d007`  
		Last Modified: Thu, 23 Jul 2020 05:41:12 GMT  
		Size: 100.3 MB (100344362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aead886d739bd3bc027292813e19b942521fd83e2b87b84d7ffc57cf359fd04d`  
		Last Modified: Thu, 23 Jul 2020 05:40:51 GMT  
		Size: 1.3 MB (1290010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf6afd72f85c187c4e3cd56894c0bd2fc5342847b64e204b8380d74572930c`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c518dbadfc9a2b2040e19141f943668ca44272fa3522b735d8d40966dcc238bc`  
		Last Modified: Thu, 23 Jul 2020 05:40:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b813ca710fb3e9cf25dea3c2473a35f4165a8c4d1cb4e3c1209547b4b1da26ce`  
		Last Modified: Thu, 23 Jul 2020 05:40:47 GMT  
		Size: 2.7 MB (2739767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927698c2c46c1e2009a7d99151cb2489579f4c2d2c6b43be64618a6915bff86`  
		Last Modified: Thu, 23 Jul 2020 05:40:55 GMT  
		Size: 58.4 MB (58421593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b0e2e590831a782eae54596172a684f302529c2726b8e70b6136621a7dcc83`  
		Last Modified: Thu, 23 Jul 2020 05:40:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:9cacc436f5e29968b595f56a05fb9a85d8cf599ad03ff9e513f249d68d9e2b1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210720601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84be3ab4689f85e4e730235b2d5605c6aed59471c02fa85ef7d8370f46a85d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:26:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 04 Aug 2020 05:26:52 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_MAJOR=2.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_VERSION=2.6.6
# Tue, 04 Aug 2020 05:37:07 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Tue, 04 Aug 2020 05:38:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 04 Aug 2020 05:38:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 04 Aug 2020 05:38:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:38:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 04 Aug 2020 05:38:37 GMT
CMD ["irb"]
# Tue, 04 Aug 2020 11:06:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 04 Aug 2020 11:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:07:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:07:31 GMT
ENV RAILS_ENV=production
# Tue, 04 Aug 2020 11:07:31 GMT
WORKDIR /usr/src/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
ENV HOME=/home/redmine
# Tue, 04 Aug 2020 11:07:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 04 Aug 2020 11:07:32 GMT
ENV REDMINE_VERSION=4.1.1
# Tue, 04 Aug 2020 11:07:33 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Tue, 04 Aug 2020 11:07:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 04 Aug 2020 11:09:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 11:09:19 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 04 Aug 2020 11:09:19 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Tue, 04 Aug 2020 11:09:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 11:09:19 GMT
EXPOSE 3000
# Tue, 04 Aug 2020 11:09:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583e211a076d7bec7a39d1bc35ccd2ecfb97ecad9d15942b454d420c015aec78`  
		Last Modified: Tue, 04 Aug 2020 05:43:18 GMT  
		Size: 10.8 MB (10796400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea16a6f63db965daa21205a21bc3d56b39bc5415cb4fc0fbd4adc06bf68dbf`  
		Last Modified: Tue, 04 Aug 2020 05:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652803a9a3f37b5c0eb597d3cb545de4faeb3c8a0777c699a3b469318679edfc`  
		Last Modified: Tue, 04 Aug 2020 05:43:40 GMT  
		Size: 21.6 MB (21597298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661376aa0be2fb0f0f21b27678f8b46875aae059d564c4315df9156902b3fc58`  
		Last Modified: Tue, 04 Aug 2020 05:43:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9663cc42a0bb2db620a9f95bf2eac90ab8bb99edc3270b24130730ac855079`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4fee1c0fdf6aa4e3bdf1ad574569cc4b91918ecccf3121781b6222a536c493`  
		Last Modified: Tue, 04 Aug 2020 11:13:14 GMT  
		Size: 90.9 MB (90854185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a738a595cfdd936a270ac3a839188391d9a832eb23a682df205b380edef952`  
		Last Modified: Tue, 04 Aug 2020 11:13:01 GMT  
		Size: 1.4 MB (1355115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4ded94c32cc1762576dc5d1895c8ff2a61981a4b18f844ab529a5bc3f11a60`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4fc727b1933c0c8e1ec90802948f0caa3068693f5edc86e07fc249ba40c9c7`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9d70d6ba3b29079423c01dae21a4f44b5de6687dc28b84909413ddf4de164f`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.7 MB (2739769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5248a897bfb0f149c6c341f108ecccd52d07ffd97ed1aeea3bf0872bf4654f`  
		Last Modified: Tue, 04 Aug 2020 11:13:05 GMT  
		Size: 57.7 MB (57665687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaad00d5183f9814d6f3c76d671245eff35857f941e9587960a79408ae0116e`  
		Last Modified: Tue, 04 Aug 2020 11:12:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:03d9af0c2ca87b7616d4840215153c2e197e90ffb688aaa7d4256a9522bbb6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:b6ac2a73471e47140756a2b13d76ecdaa35f73d2d7cae6c9bb3190752ee5c891
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241044548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd51b224bd422e274789598472d83448ec2875abfe851e232ad9c8797baecc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 21:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:18:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 21:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 21:27:40 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 21:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 21:32:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 21:32:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 21:32:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 21:32:25 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 07:36:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 23 Jul 2020 07:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 07:37:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:37:02 GMT
ENV RAILS_ENV=production
# Thu, 23 Jul 2020 07:37:03 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
ENV HOME=/home/redmine
# Thu, 23 Jul 2020 07:37:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_VERSION=4.1.1
# Thu, 23 Jul 2020 07:37:04 GMT
ENV REDMINE_DOWNLOAD_MD5=a15a25dec7b866e213bbd4b041f05f17
# Thu, 23 Jul 2020 07:37:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 23 Jul 2020 07:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:38:42 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jul 2020 07:38:42 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Thu, 23 Jul 2020 07:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 07:38:42 GMT
EXPOSE 3000
# Thu, 23 Jul 2020 07:38:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 23 Jul 2020 07:38:57 GMT
ENV PASSENGER_VERSION=6.0.6
# Thu, 23 Jul 2020 07:39:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jul 2020 07:39:15 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 23 Jul 2020 07:39:15 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 23 Jul 2020 07:39:15 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c307964a7468ebde2c011ff4545d603192f4cd5dc22631275238be87764b64bc`  
		Last Modified: Wed, 22 Jul 2020 21:54:21 GMT  
		Size: 12.5 MB (12539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2d286493ebb13cac631e5147f3b4f76567edfa8580935e5af161dc65e8a43a`  
		Last Modified: Wed, 22 Jul 2020 21:54:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf773e09df35aec5cd43aa6220c0a4c6126cc336460b0c6cf2be72613afa6406`  
		Last Modified: Wed, 22 Jul 2020 21:54:41 GMT  
		Size: 21.5 MB (21450342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41f225850f3de55d2002487f7a14ef6bf5a85d312ca9e9dc3f644b665a34362`  
		Last Modified: Wed, 22 Jul 2020 21:54:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fa7c9620c64c5a82e96ac5b020cee1b7b78ff3852ff7fd859ba90304fc3e3d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bca7298389e0a7d806d1b8632181e984e0f7d84f9bbe734c63300f9f2afd1a`  
		Last Modified: Thu, 23 Jul 2020 07:43:23 GMT  
		Size: 93.1 MB (93108726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af857119c943f7187bdf0f29aab9a195a9c2875326e22d4866799d636ce323`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 1.4 MB (1369455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1c6ad5d29340e67cbd956a9ad712e76ff848a230840913f212e3092d7c345b`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed9a8222ad48c340e21883c406f32555719c0a0da8bef356cb510862231072`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a2de0559edc613cc682061c5ea170f89a4c9ddff4348b15be9a6ca5764f5d`  
		Last Modified: Thu, 23 Jul 2020 07:43:06 GMT  
		Size: 2.7 MB (2739483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1eb2d25805c191d8607d87423cdf6756b5cebcf74f9a17e54d7643b00f19e5`  
		Last Modified: Thu, 23 Jul 2020 07:43:14 GMT  
		Size: 57.9 MB (57861637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4bebd31d6fc0be0d851517ef2f806b9c15365bd3b954424c606563624b9e`  
		Last Modified: Thu, 23 Jul 2020 07:43:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99902f714402485f8d8b64277c5572d9a10ada60e58740726e237d8b48187d19`  
		Last Modified: Thu, 23 Jul 2020 07:43:31 GMT  
		Size: 20.0 MB (19952240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d01d908740d1afae692b875052e99be2e6fc83c460822b7b8109614ada45a5`  
		Last Modified: Thu, 23 Jul 2020 07:43:29 GMT  
		Size: 4.9 MB (4920453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
