<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redmine`

-	[`redmine:3`](#redmine3)
-	[`redmine:3.4`](#redmine34)
-	[`redmine:3.4.13`](#redmine3413)
-	[`redmine:3.4.13-alpine`](#redmine3413-alpine)
-	[`redmine:3.4.13-passenger`](#redmine3413-passenger)
-	[`redmine:3.4-alpine`](#redmine34-alpine)
-	[`redmine:3.4-passenger`](#redmine34-passenger)
-	[`redmine:3-alpine`](#redmine3-alpine)
-	[`redmine:3-passenger`](#redmine3-passenger)
-	[`redmine:4`](#redmine4)
-	[`redmine:4.0`](#redmine40)
-	[`redmine:4.0.6`](#redmine406)
-	[`redmine:4.0.6-alpine`](#redmine406-alpine)
-	[`redmine:4.0.6-passenger`](#redmine406-passenger)
-	[`redmine:4.0-alpine`](#redmine40-alpine)
-	[`redmine:4.0-passenger`](#redmine40-passenger)
-	[`redmine:4.1`](#redmine41)
-	[`redmine:4.1.0`](#redmine410)
-	[`redmine:4.1.0-alpine`](#redmine410-alpine)
-	[`redmine:4.1.0-passenger`](#redmine410-passenger)
-	[`redmine:4.1-alpine`](#redmine41-alpine)
-	[`redmine:4.1-passenger`](#redmine41-passenger)
-	[`redmine:4-alpine`](#redmine4-alpine)
-	[`redmine:4-passenger`](#redmine4-passenger)
-	[`redmine:alpine`](#redminealpine)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:3`

```console
$ docker pull redmine@sha256:c3b025ec0a086a2a4b48bc448cdcbedacc0a24a2ee4ba2104bc09a1f18e6917e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3` - linux; amd64

```console
$ docker pull redmine@sha256:175859dad6954137fdc98d3f9c2a3d65e2a09c95a69d59dc012fda34077a53df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207376944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e876f5c03ce2cb606556af03d69808239c091cf094883b081a0704a51f99ebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:46:08 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 07:51:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:51:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:51:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:51:35 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:11:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:42 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:11:43 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:11:43 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 23:11:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:04 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:14:04 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:14:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:14:05 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:14:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786668394d8864c32001fe2e017691a48e2586962ddadbdd89f3ed1ae3a581b`  
		Last Modified: Sun, 02 Feb 2020 08:05:23 GMT  
		Size: 22.0 MB (22005923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60eeb2d371f01868f9ef2b98cba4e5e4931d7d7f39c22836a1475d47eaa8f79`  
		Last Modified: Sun, 02 Feb 2020 08:05:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0373bcbc7b2dab8ac9a9ba9ece619ebb6ca62092225d55d4d8d78cd9202719`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eca2f7a07b7dea7ab03816feab6eeffd3d7478df839e48b849feea6398c224`  
		Last Modified: Sun, 02 Feb 2020 23:16:04 GMT  
		Size: 80.2 MB (80156868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbf8bf952bb8dfb4b3d541f4bba137a571525745351c08c5e54cedca086bd5`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.3 MB (1296462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082b3c4f84767770e61ac8e821a5ee44d0e983efbf8b13e4e4aab4d6e3bc9866`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e42467cf2f62990f02e9212aec38ba28e25dca180264cea0a88b2007291aeb9`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b75b5408489e6f25990040f1b8471eb98fa14939ed17dd6ca30fc5ac11717`  
		Last Modified: Sun, 02 Feb 2020 23:15:45 GMT  
		Size: 2.5 MB (2463472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85556fa4b9beeefeb0f9d07cc9838902d1817ee7067626c1d8b92e1ef9e08ad5`  
		Last Modified: Sun, 02 Feb 2020 23:16:09 GMT  
		Size: 61.8 MB (61817813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520906d2d3e8676e38f024b4844415f16350c5b7ef11d97e61cc6f1d6ca39148`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; arm variant v5

```console
$ docker pull redmine@sha256:c94aeafc4839953ffc6f1d091d0be07f4b08b8798aac09ad6d5553bccf4919f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197297445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cd43b3d587718da99aba51d70195446f839e60ec885836249565df5fa1e5f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:53:06 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 02:53:07 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 02:53:07 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 02:53:08 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 03:00:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:00:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:00:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:00:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:00:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:00:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:58:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:00:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:00:16 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 10:00:17 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 10:00:18 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 10:00:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 10:00:24 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 10:00:26 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 10:00:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 10:06:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:06:54 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 10:06:55 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 10:06:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 10:06:56 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 10:06:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9d66a1f914bdc48f10a9fb7fa826de1fc4d51127360bfb635de92800427c2c`  
		Last Modified: Sun, 02 Feb 2020 03:18:21 GMT  
		Size: 21.3 MB (21337996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59db49767202ac506ef64e9ad4e78c2222a92d585fc752c47494f69c8d66c40`  
		Last Modified: Sun, 02 Feb 2020 03:18:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb41ba2542818a91d69186164d2baa8245ac6afcfb94f1fcb0d6f6e512d1065`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd4d2b24e257beb61f33391e5e90e9967dc45a757e66afcf682f086ae1db02b`  
		Last Modified: Sun, 02 Feb 2020 10:09:15 GMT  
		Size: 76.0 MB (76036604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774123ad6534a0960d229fc9293ab82687ff0eb673ef39fe99574fdb43fc0300`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 1.3 MB (1254237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba04482a10d8e7ec8a828448873ef5521cb469231897b4757a6e3acb3772cce`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a493edaaf61e6e3d79bca713573cd3eada2ce4a0149ce264e8c82f1a087b407`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943138c7822bb22264d257ee437bf08d764d088aca0a6279ba23f62232241da4`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfefd54730a9b78dff4a21cc9482ecaa0526bbced5ccd32add28fead591f587`  
		Last Modified: Sun, 02 Feb 2020 10:08:55 GMT  
		Size: 61.0 MB (61044490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bbf1e5c954dbffe8437807f7327f66456bb1c60539fbea8fd822d16dcdfb2f`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; arm variant v7

```console
$ docker pull redmine@sha256:881d1780e71108b5411563601467d378fbb2b121328d6aa9000281f00b52db15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190681440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6968e193bed06b26318c8451aa7afc3c230fbac500a27414d224035a8c7b79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 04:17:15 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 04:17:16 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 04:17:16 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 04:17:17 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 04:23:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 04:23:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 04:23:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 04:23:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 04:23:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 04:23:28 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:35:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:36:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:36:39 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:36:41 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:36:41 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:36:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 18:36:45 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 18:36:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:41:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:41:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:41:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:41:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:41:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:41:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07d29d58da63af2cbe4b2634cbe59f64f36f3e0066cb408f5a2edd98e053034`  
		Last Modified: Sun, 02 Feb 2020 04:40:15 GMT  
		Size: 21.3 MB (21261285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237d4c157ad8e1b0ecbd7678efa8e6b0108df89c7884953e10b971e43222aeea`  
		Last Modified: Sun, 02 Feb 2020 04:40:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0bf238bc883cfcaa3a941ab1b0f83f4ce91332331d703dd4949c2b2261a3c6`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86c1bbd379b656ef6c9d3f742413f0c57faa2904e2a30d715d399a94c70e86b`  
		Last Modified: Sun, 02 Feb 2020 18:43:48 GMT  
		Size: 72.4 MB (72380570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c79ca0fe8317fe54ec51b24b536a24abd0cb9e370ff2dcbdadb1532c3245`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 1.2 MB (1243624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be178bdea130e3af4f2130f197714194a65659e0395e72fdef183eaed592185`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d774b53991a65afa639c84acf0402ff90cab523241a2d3ad7df5645135f3b6dc`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79eb6ad64482bcdea621eba462b32a5f797b655d4c0018be01e8a65048cc0a2a`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a37ce0d23a5af8c1f74f177c52941751acca22a5ee59e8072956eb17e572`  
		Last Modified: Sun, 02 Feb 2020 18:43:43 GMT  
		Size: 60.8 MB (60781105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38809f370b0079b82eac7e830b034bf6da09c943e9063536585dfe7c2e78f25`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e8eafd596a79c22008bf82469fa3776b70dedd1179fdd95419314f54a8fc6611
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203238173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a5ded75bfd43a680e9286ad2f2ec09176be76c4f886d02013e7021490e1c40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:36:56 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 10:36:57 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 10:36:57 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 10:36:58 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 10:43:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:43:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:43:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:43:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:43:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:43:43 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:42:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:43:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:43:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:43:50 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:43:51 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:43:52 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:43:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:43:54 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 19:43:54 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 19:43:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:48:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:49:02 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:49:03 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:49:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:49:04 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:49:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ec78c9827c04b80b760ede68bd7175ac30c50c3affbcdb1a54ce990efc340b`  
		Last Modified: Sun, 02 Feb 2020 11:00:05 GMT  
		Size: 21.9 MB (21879217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8ca927e3b9d45908aebe55722c4cd52f0f7dd9bde47c04b8d54aa3724fbb1`  
		Last Modified: Sun, 02 Feb 2020 10:59:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0114a7f90ce24be9c49676ce7650984bc656655cab4d7058d383138ef4bb314d`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb1a386ed4531d7b8ec2c3f5672f9d9c1411be1ad3cf6a95864cb312e89732`  
		Last Modified: Sun, 02 Feb 2020 19:50:53 GMT  
		Size: 78.8 MB (78782615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8578be9b1680f572739cfc6db25ed6501ade895ebc5e30d0634849b0cb238f`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 1.2 MB (1228534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddb3dbc651e684524e1c65ad1e308b834114428efd28784676ed63c9ff7949a`  
		Last Modified: Sun, 02 Feb 2020 19:50:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96574221c0c841bc66a9c26f2ed08aa6e31a742ed05fa152d8f44251abdcbadf`  
		Last Modified: Sun, 02 Feb 2020 19:50:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc4d9969e9404b689c5f8740b9311243bf3407c2c69b2db48df55c84ca7325a`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb009ed80778f7856c88a80a232596f3e5b9183ff37533f79ac44403c559b12`  
		Last Modified: Sun, 02 Feb 2020 19:50:43 GMT  
		Size: 61.8 MB (61784273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fe2169ada7bbb90d8d5bf5dc65b065e6e36f39d252bacc7005f57301a3fc0f`  
		Last Modified: Sun, 02 Feb 2020 19:50:28 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; 386

```console
$ docker pull redmine@sha256:d86ad9bb76b50667b6d81f9627bd8a34987643c2e20d8214acc4803d54579a00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212835313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaad5817352379ddf843b931d215edab162f606ec5740ef6e4328a30565689f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:22:47 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 10:22:47 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 10:22:48 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 10:22:48 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 10:27:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:28:01 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:22:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:23:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:23:34 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:23:35 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:23:35 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:23:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:23:36 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 13:23:36 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 13:23:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:27:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:27:45 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:27:45 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:27:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:27:46 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:27:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deceb1d6937dd7c5ab8da8ae625647600eaf912e5e42cf7ce805cd7368314bf5`  
		Last Modified: Sun, 02 Feb 2020 10:41:40 GMT  
		Size: 21.5 MB (21545842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43f910fc95479ba6ffe8b02c62974b994bc60e437b10f72d578216b3c934760`  
		Last Modified: Sun, 02 Feb 2020 10:41:36 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672e8d6d4b2a4232841a34d3de7de9005d4a58d98bd7a8ce2e22601d7e026ef`  
		Last Modified: Sun, 02 Feb 2020 13:29:47 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dda6b5b351f4fa6001502299225a2686b84d135fccef81ec3782e4354456a26`  
		Last Modified: Sun, 02 Feb 2020 13:30:21 GMT  
		Size: 81.6 MB (81576493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87417673835a9f2eb395fedbc3789bba85e7957368b9082ad3d7ede0e1be118`  
		Last Modified: Sun, 02 Feb 2020 13:29:47 GMT  
		Size: 1.3 MB (1261019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8eae15c841c71cb6dcd54aae44a8c1de016254e47a3d11fbb37137079b7b00`  
		Last Modified: Sun, 02 Feb 2020 13:29:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973b03ec9c77ef337237646ab70e4bec2b2184bf0f215c3b54753677af78b324`  
		Last Modified: Sun, 02 Feb 2020 13:29:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c370993c1d07a839073931227cae7763db464e4d79b9801e81da36a0a180ae6`  
		Last Modified: Sun, 02 Feb 2020 13:29:48 GMT  
		Size: 2.5 MB (2463471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9fd27bcf3d2044038a7c06fee4626de3f4508af27c329214b69a0806528e6d`  
		Last Modified: Sun, 02 Feb 2020 13:30:04 GMT  
		Size: 61.0 MB (61031067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501022e56770ca5e6c01e546d5079e0da4a0ace3aafe9c926a105d9f008c6f9c`  
		Last Modified: Sun, 02 Feb 2020 13:29:46 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; ppc64le

```console
$ docker pull redmine@sha256:92d2d235dc43a433721f8987c4d9d024bb265748afd2deaee6230f6bad213e04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218599690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734128e8f923729da55c4a99bbbfc57e619a2481ccf170c04667cc85a3b5c376`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:56:58 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:57:05 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:57:08 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:57:12 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 08:04:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 08:04:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 08:04:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 08:04:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 08:05:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 08:05:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:40:07 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:43:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:43:11 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:43:14 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:43:16 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:43:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:43:25 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 16:43:27 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 16:43:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:52:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:52:14 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:52:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:52:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:52:20 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:52:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d12304aa6631ac8d42bf1efbf18f76ea3aeff54abba871917165fd259590e6a`  
		Last Modified: Sun, 02 Feb 2020 08:22:34 GMT  
		Size: 22.5 MB (22518893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858322931e6addd835a834cfa5f022232aa257884c1b3b6df9a2f98905b4cd8`  
		Last Modified: Sun, 02 Feb 2020 08:22:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9239b7306ba44ba946d71ae6282bece91bf0792f996cfe99f46ecda2e288b67`  
		Last Modified: Sun, 02 Feb 2020 16:54:00 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f19cd445a9633a3d3fe7d1d3655305e713846023a23ca193cd3fa45e480fcd`  
		Last Modified: Sun, 02 Feb 2020 16:54:18 GMT  
		Size: 86.9 MB (86851603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5496c125aafc5dfc36800a42072774716b1e523b9d96c22824f417264aeba8d8`  
		Last Modified: Sun, 02 Feb 2020 16:53:59 GMT  
		Size: 1.2 MB (1218419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725e9a597dacd2e94b50e226c3b439764c8119cfb6620d6ea048d14d532dab17`  
		Last Modified: Sun, 02 Feb 2020 16:53:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1a18583c13a8b1f51cbaf9f28be0eafd0b3276de46c10c1e7288d4a69ab6d9`  
		Last Modified: Sun, 02 Feb 2020 16:53:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167104d9121defa8cce0b59d169692412b788237a4e9f948b985a5ada11f391`  
		Last Modified: Sun, 02 Feb 2020 16:53:57 GMT  
		Size: 2.5 MB (2463875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c515c0b2c89b7d42b7c7807760beef5c71d04eb4277f3c1a08745feca852f4`  
		Last Modified: Sun, 02 Feb 2020 16:54:09 GMT  
		Size: 62.3 MB (62335852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f37a8e2e2e4693a5d834b1e5a4f8f568608351713b882ebeb076e99eab8bb5`  
		Last Modified: Sun, 02 Feb 2020 16:53:55 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; s390x

```console
$ docker pull redmine@sha256:2370a4642f404adbcdd7c37975e2aa8a4a9c399593cf21b831a7753bf31f1fd2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202577034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889f0b16b19300fc0a24e1c00746a0ab8ffe37e3001f3e859a8832c7e724ffeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:48:48 GMT
ENV RUBY_MAJOR=2.4
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBY_VERSION=2.4.9
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sat, 01 Feb 2020 22:51:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:51:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:51:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:51:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:51:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:51:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:31:52 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:32:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:32:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:32:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:32:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:32:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:32:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:32:26 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 03:32:26 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 03:32:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:34:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:34:39 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:34:39 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:34:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:34:39 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:34:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace099387f5254edf276126e046611f26609fd7b03c6eccab25882e8492ab41f`  
		Last Modified: Sat, 01 Feb 2020 22:58:36 GMT  
		Size: 22.2 MB (22151592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b170fa9fa8c788d38c6d6505a94b57d409b33565fd70320c01ce2c1a22977c6`  
		Last Modified: Sat, 01 Feb 2020 22:58:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8b559eb775e7ef2268ad21235635a36ac961841bf8d21ff310f414a71c80e`  
		Last Modified: Sun, 02 Feb 2020 03:36:10 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeaef2a78b559791011534abf0ee2a723b138776372b00019af6f1bcf1b59da`  
		Last Modified: Sun, 02 Feb 2020 03:36:21 GMT  
		Size: 77.9 MB (77940591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf387e3c6ea73ebb6cd13db382724dff9771329e421c8c4ed454fe11927aea0e`  
		Last Modified: Sun, 02 Feb 2020 03:36:09 GMT  
		Size: 1.3 MB (1283198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662f8c8a715db4b4d679682f19697f18f3d11ce144ca00a77c43d87f8251198e`  
		Last Modified: Sun, 02 Feb 2020 03:36:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d75b229dcd884bd3aa4e230e09890af1beccdf1e73b531fdfef09787a956f`  
		Last Modified: Sun, 02 Feb 2020 03:36:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e04af6349cfcff77309336b34350e8fd67956803fe9408f9ff99f121eb6f15`  
		Last Modified: Sun, 02 Feb 2020 03:36:09 GMT  
		Size: 2.5 MB (2463866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babe457f5e43177a09c215741217f93c7a724ca2a67b1bbd2b2ae33bc8e96108`  
		Last Modified: Sun, 02 Feb 2020 03:36:29 GMT  
		Size: 62.2 MB (62231901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9a86c32d5039b929295c3d0162a1177253345f3654fb1e75ddba4477957176`  
		Last Modified: Sun, 02 Feb 2020 03:36:39 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4`

```console
$ docker pull redmine@sha256:c3b025ec0a086a2a4b48bc448cdcbedacc0a24a2ee4ba2104bc09a1f18e6917e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.4` - linux; amd64

```console
$ docker pull redmine@sha256:175859dad6954137fdc98d3f9c2a3d65e2a09c95a69d59dc012fda34077a53df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207376944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e876f5c03ce2cb606556af03d69808239c091cf094883b081a0704a51f99ebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:46:08 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 07:51:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:51:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:51:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:51:35 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:11:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:42 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:11:43 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:11:43 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 23:11:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:04 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:14:04 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:14:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:14:05 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:14:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786668394d8864c32001fe2e017691a48e2586962ddadbdd89f3ed1ae3a581b`  
		Last Modified: Sun, 02 Feb 2020 08:05:23 GMT  
		Size: 22.0 MB (22005923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60eeb2d371f01868f9ef2b98cba4e5e4931d7d7f39c22836a1475d47eaa8f79`  
		Last Modified: Sun, 02 Feb 2020 08:05:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0373bcbc7b2dab8ac9a9ba9ece619ebb6ca62092225d55d4d8d78cd9202719`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eca2f7a07b7dea7ab03816feab6eeffd3d7478df839e48b849feea6398c224`  
		Last Modified: Sun, 02 Feb 2020 23:16:04 GMT  
		Size: 80.2 MB (80156868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbf8bf952bb8dfb4b3d541f4bba137a571525745351c08c5e54cedca086bd5`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.3 MB (1296462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082b3c4f84767770e61ac8e821a5ee44d0e983efbf8b13e4e4aab4d6e3bc9866`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e42467cf2f62990f02e9212aec38ba28e25dca180264cea0a88b2007291aeb9`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b75b5408489e6f25990040f1b8471eb98fa14939ed17dd6ca30fc5ac11717`  
		Last Modified: Sun, 02 Feb 2020 23:15:45 GMT  
		Size: 2.5 MB (2463472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85556fa4b9beeefeb0f9d07cc9838902d1817ee7067626c1d8b92e1ef9e08ad5`  
		Last Modified: Sun, 02 Feb 2020 23:16:09 GMT  
		Size: 61.8 MB (61817813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520906d2d3e8676e38f024b4844415f16350c5b7ef11d97e61cc6f1d6ca39148`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:c94aeafc4839953ffc6f1d091d0be07f4b08b8798aac09ad6d5553bccf4919f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197297445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cd43b3d587718da99aba51d70195446f839e60ec885836249565df5fa1e5f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:53:06 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 02:53:07 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 02:53:07 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 02:53:08 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 03:00:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:00:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:00:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:00:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:00:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:00:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:58:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:00:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:00:16 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 10:00:17 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 10:00:18 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 10:00:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 10:00:24 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 10:00:26 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 10:00:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 10:06:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:06:54 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 10:06:55 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 10:06:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 10:06:56 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 10:06:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9d66a1f914bdc48f10a9fb7fa826de1fc4d51127360bfb635de92800427c2c`  
		Last Modified: Sun, 02 Feb 2020 03:18:21 GMT  
		Size: 21.3 MB (21337996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59db49767202ac506ef64e9ad4e78c2222a92d585fc752c47494f69c8d66c40`  
		Last Modified: Sun, 02 Feb 2020 03:18:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb41ba2542818a91d69186164d2baa8245ac6afcfb94f1fcb0d6f6e512d1065`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd4d2b24e257beb61f33391e5e90e9967dc45a757e66afcf682f086ae1db02b`  
		Last Modified: Sun, 02 Feb 2020 10:09:15 GMT  
		Size: 76.0 MB (76036604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774123ad6534a0960d229fc9293ab82687ff0eb673ef39fe99574fdb43fc0300`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 1.3 MB (1254237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba04482a10d8e7ec8a828448873ef5521cb469231897b4757a6e3acb3772cce`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a493edaaf61e6e3d79bca713573cd3eada2ce4a0149ce264e8c82f1a087b407`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943138c7822bb22264d257ee437bf08d764d088aca0a6279ba23f62232241da4`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfefd54730a9b78dff4a21cc9482ecaa0526bbced5ccd32add28fead591f587`  
		Last Modified: Sun, 02 Feb 2020 10:08:55 GMT  
		Size: 61.0 MB (61044490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bbf1e5c954dbffe8437807f7327f66456bb1c60539fbea8fd822d16dcdfb2f`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:881d1780e71108b5411563601467d378fbb2b121328d6aa9000281f00b52db15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190681440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6968e193bed06b26318c8451aa7afc3c230fbac500a27414d224035a8c7b79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 04:17:15 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 04:17:16 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 04:17:16 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 04:17:17 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 04:23:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 04:23:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 04:23:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 04:23:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 04:23:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 04:23:28 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:35:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:36:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:36:39 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:36:41 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:36:41 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:36:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 18:36:45 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 18:36:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:41:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:41:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:41:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:41:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:41:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:41:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07d29d58da63af2cbe4b2634cbe59f64f36f3e0066cb408f5a2edd98e053034`  
		Last Modified: Sun, 02 Feb 2020 04:40:15 GMT  
		Size: 21.3 MB (21261285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237d4c157ad8e1b0ecbd7678efa8e6b0108df89c7884953e10b971e43222aeea`  
		Last Modified: Sun, 02 Feb 2020 04:40:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0bf238bc883cfcaa3a941ab1b0f83f4ce91332331d703dd4949c2b2261a3c6`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86c1bbd379b656ef6c9d3f742413f0c57faa2904e2a30d715d399a94c70e86b`  
		Last Modified: Sun, 02 Feb 2020 18:43:48 GMT  
		Size: 72.4 MB (72380570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c79ca0fe8317fe54ec51b24b536a24abd0cb9e370ff2dcbdadb1532c3245`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 1.2 MB (1243624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be178bdea130e3af4f2130f197714194a65659e0395e72fdef183eaed592185`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d774b53991a65afa639c84acf0402ff90cab523241a2d3ad7df5645135f3b6dc`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79eb6ad64482bcdea621eba462b32a5f797b655d4c0018be01e8a65048cc0a2a`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a37ce0d23a5af8c1f74f177c52941751acca22a5ee59e8072956eb17e572`  
		Last Modified: Sun, 02 Feb 2020 18:43:43 GMT  
		Size: 60.8 MB (60781105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38809f370b0079b82eac7e830b034bf6da09c943e9063536585dfe7c2e78f25`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e8eafd596a79c22008bf82469fa3776b70dedd1179fdd95419314f54a8fc6611
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203238173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a5ded75bfd43a680e9286ad2f2ec09176be76c4f886d02013e7021490e1c40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:36:56 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 10:36:57 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 10:36:57 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 10:36:58 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 10:43:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:43:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:43:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:43:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:43:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:43:43 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:42:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:43:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:43:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:43:50 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:43:51 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:43:52 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:43:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:43:54 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 19:43:54 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 19:43:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:48:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:49:02 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:49:03 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:49:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:49:04 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:49:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ec78c9827c04b80b760ede68bd7175ac30c50c3affbcdb1a54ce990efc340b`  
		Last Modified: Sun, 02 Feb 2020 11:00:05 GMT  
		Size: 21.9 MB (21879217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8ca927e3b9d45908aebe55722c4cd52f0f7dd9bde47c04b8d54aa3724fbb1`  
		Last Modified: Sun, 02 Feb 2020 10:59:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0114a7f90ce24be9c49676ce7650984bc656655cab4d7058d383138ef4bb314d`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb1a386ed4531d7b8ec2c3f5672f9d9c1411be1ad3cf6a95864cb312e89732`  
		Last Modified: Sun, 02 Feb 2020 19:50:53 GMT  
		Size: 78.8 MB (78782615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8578be9b1680f572739cfc6db25ed6501ade895ebc5e30d0634849b0cb238f`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 1.2 MB (1228534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddb3dbc651e684524e1c65ad1e308b834114428efd28784676ed63c9ff7949a`  
		Last Modified: Sun, 02 Feb 2020 19:50:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96574221c0c841bc66a9c26f2ed08aa6e31a742ed05fa152d8f44251abdcbadf`  
		Last Modified: Sun, 02 Feb 2020 19:50:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc4d9969e9404b689c5f8740b9311243bf3407c2c69b2db48df55c84ca7325a`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb009ed80778f7856c88a80a232596f3e5b9183ff37533f79ac44403c559b12`  
		Last Modified: Sun, 02 Feb 2020 19:50:43 GMT  
		Size: 61.8 MB (61784273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fe2169ada7bbb90d8d5bf5dc65b065e6e36f39d252bacc7005f57301a3fc0f`  
		Last Modified: Sun, 02 Feb 2020 19:50:28 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; 386

```console
$ docker pull redmine@sha256:d86ad9bb76b50667b6d81f9627bd8a34987643c2e20d8214acc4803d54579a00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212835313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaad5817352379ddf843b931d215edab162f606ec5740ef6e4328a30565689f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:22:47 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 10:22:47 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 10:22:48 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 10:22:48 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 10:27:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:28:01 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:22:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:23:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:23:34 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:23:35 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:23:35 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:23:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:23:36 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 13:23:36 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 13:23:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:27:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:27:45 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:27:45 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:27:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:27:46 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:27:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deceb1d6937dd7c5ab8da8ae625647600eaf912e5e42cf7ce805cd7368314bf5`  
		Last Modified: Sun, 02 Feb 2020 10:41:40 GMT  
		Size: 21.5 MB (21545842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43f910fc95479ba6ffe8b02c62974b994bc60e437b10f72d578216b3c934760`  
		Last Modified: Sun, 02 Feb 2020 10:41:36 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672e8d6d4b2a4232841a34d3de7de9005d4a58d98bd7a8ce2e22601d7e026ef`  
		Last Modified: Sun, 02 Feb 2020 13:29:47 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dda6b5b351f4fa6001502299225a2686b84d135fccef81ec3782e4354456a26`  
		Last Modified: Sun, 02 Feb 2020 13:30:21 GMT  
		Size: 81.6 MB (81576493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87417673835a9f2eb395fedbc3789bba85e7957368b9082ad3d7ede0e1be118`  
		Last Modified: Sun, 02 Feb 2020 13:29:47 GMT  
		Size: 1.3 MB (1261019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8eae15c841c71cb6dcd54aae44a8c1de016254e47a3d11fbb37137079b7b00`  
		Last Modified: Sun, 02 Feb 2020 13:29:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973b03ec9c77ef337237646ab70e4bec2b2184bf0f215c3b54753677af78b324`  
		Last Modified: Sun, 02 Feb 2020 13:29:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c370993c1d07a839073931227cae7763db464e4d79b9801e81da36a0a180ae6`  
		Last Modified: Sun, 02 Feb 2020 13:29:48 GMT  
		Size: 2.5 MB (2463471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9fd27bcf3d2044038a7c06fee4626de3f4508af27c329214b69a0806528e6d`  
		Last Modified: Sun, 02 Feb 2020 13:30:04 GMT  
		Size: 61.0 MB (61031067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501022e56770ca5e6c01e546d5079e0da4a0ace3aafe9c926a105d9f008c6f9c`  
		Last Modified: Sun, 02 Feb 2020 13:29:46 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; ppc64le

```console
$ docker pull redmine@sha256:92d2d235dc43a433721f8987c4d9d024bb265748afd2deaee6230f6bad213e04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218599690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734128e8f923729da55c4a99bbbfc57e619a2481ccf170c04667cc85a3b5c376`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:56:58 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:57:05 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:57:08 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:57:12 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 08:04:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 08:04:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 08:04:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 08:04:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 08:05:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 08:05:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:40:07 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:43:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:43:11 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:43:14 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:43:16 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:43:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:43:25 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 16:43:27 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 16:43:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:52:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:52:14 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:52:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:52:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:52:20 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:52:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d12304aa6631ac8d42bf1efbf18f76ea3aeff54abba871917165fd259590e6a`  
		Last Modified: Sun, 02 Feb 2020 08:22:34 GMT  
		Size: 22.5 MB (22518893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858322931e6addd835a834cfa5f022232aa257884c1b3b6df9a2f98905b4cd8`  
		Last Modified: Sun, 02 Feb 2020 08:22:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9239b7306ba44ba946d71ae6282bece91bf0792f996cfe99f46ecda2e288b67`  
		Last Modified: Sun, 02 Feb 2020 16:54:00 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f19cd445a9633a3d3fe7d1d3655305e713846023a23ca193cd3fa45e480fcd`  
		Last Modified: Sun, 02 Feb 2020 16:54:18 GMT  
		Size: 86.9 MB (86851603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5496c125aafc5dfc36800a42072774716b1e523b9d96c22824f417264aeba8d8`  
		Last Modified: Sun, 02 Feb 2020 16:53:59 GMT  
		Size: 1.2 MB (1218419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725e9a597dacd2e94b50e226c3b439764c8119cfb6620d6ea048d14d532dab17`  
		Last Modified: Sun, 02 Feb 2020 16:53:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1a18583c13a8b1f51cbaf9f28be0eafd0b3276de46c10c1e7288d4a69ab6d9`  
		Last Modified: Sun, 02 Feb 2020 16:53:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167104d9121defa8cce0b59d169692412b788237a4e9f948b985a5ada11f391`  
		Last Modified: Sun, 02 Feb 2020 16:53:57 GMT  
		Size: 2.5 MB (2463875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c515c0b2c89b7d42b7c7807760beef5c71d04eb4277f3c1a08745feca852f4`  
		Last Modified: Sun, 02 Feb 2020 16:54:09 GMT  
		Size: 62.3 MB (62335852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f37a8e2e2e4693a5d834b1e5a4f8f568608351713b882ebeb076e99eab8bb5`  
		Last Modified: Sun, 02 Feb 2020 16:53:55 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; s390x

```console
$ docker pull redmine@sha256:2370a4642f404adbcdd7c37975e2aa8a4a9c399593cf21b831a7753bf31f1fd2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202577034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889f0b16b19300fc0a24e1c00746a0ab8ffe37e3001f3e859a8832c7e724ffeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:48:48 GMT
ENV RUBY_MAJOR=2.4
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBY_VERSION=2.4.9
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sat, 01 Feb 2020 22:51:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:51:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:51:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:51:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:51:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:51:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:31:52 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:32:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:32:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:32:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:32:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:32:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:32:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:32:26 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 03:32:26 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 03:32:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:34:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:34:39 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:34:39 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:34:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:34:39 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:34:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace099387f5254edf276126e046611f26609fd7b03c6eccab25882e8492ab41f`  
		Last Modified: Sat, 01 Feb 2020 22:58:36 GMT  
		Size: 22.2 MB (22151592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b170fa9fa8c788d38c6d6505a94b57d409b33565fd70320c01ce2c1a22977c6`  
		Last Modified: Sat, 01 Feb 2020 22:58:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8b559eb775e7ef2268ad21235635a36ac961841bf8d21ff310f414a71c80e`  
		Last Modified: Sun, 02 Feb 2020 03:36:10 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeaef2a78b559791011534abf0ee2a723b138776372b00019af6f1bcf1b59da`  
		Last Modified: Sun, 02 Feb 2020 03:36:21 GMT  
		Size: 77.9 MB (77940591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf387e3c6ea73ebb6cd13db382724dff9771329e421c8c4ed454fe11927aea0e`  
		Last Modified: Sun, 02 Feb 2020 03:36:09 GMT  
		Size: 1.3 MB (1283198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662f8c8a715db4b4d679682f19697f18f3d11ce144ca00a77c43d87f8251198e`  
		Last Modified: Sun, 02 Feb 2020 03:36:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d75b229dcd884bd3aa4e230e09890af1beccdf1e73b531fdfef09787a956f`  
		Last Modified: Sun, 02 Feb 2020 03:36:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e04af6349cfcff77309336b34350e8fd67956803fe9408f9ff99f121eb6f15`  
		Last Modified: Sun, 02 Feb 2020 03:36:09 GMT  
		Size: 2.5 MB (2463866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babe457f5e43177a09c215741217f93c7a724ca2a67b1bbd2b2ae33bc8e96108`  
		Last Modified: Sun, 02 Feb 2020 03:36:29 GMT  
		Size: 62.2 MB (62231901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9a86c32d5039b929295c3d0162a1177253345f3654fb1e75ddba4477957176`  
		Last Modified: Sun, 02 Feb 2020 03:36:39 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4.13`

```console
$ docker pull redmine@sha256:c3b025ec0a086a2a4b48bc448cdcbedacc0a24a2ee4ba2104bc09a1f18e6917e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.4.13` - linux; amd64

```console
$ docker pull redmine@sha256:175859dad6954137fdc98d3f9c2a3d65e2a09c95a69d59dc012fda34077a53df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207376944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e876f5c03ce2cb606556af03d69808239c091cf094883b081a0704a51f99ebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:46:08 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 07:51:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:51:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:51:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:51:35 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:11:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:42 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:11:43 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:11:43 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 23:11:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:04 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:14:04 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:14:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:14:05 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:14:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786668394d8864c32001fe2e017691a48e2586962ddadbdd89f3ed1ae3a581b`  
		Last Modified: Sun, 02 Feb 2020 08:05:23 GMT  
		Size: 22.0 MB (22005923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60eeb2d371f01868f9ef2b98cba4e5e4931d7d7f39c22836a1475d47eaa8f79`  
		Last Modified: Sun, 02 Feb 2020 08:05:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0373bcbc7b2dab8ac9a9ba9ece619ebb6ca62092225d55d4d8d78cd9202719`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eca2f7a07b7dea7ab03816feab6eeffd3d7478df839e48b849feea6398c224`  
		Last Modified: Sun, 02 Feb 2020 23:16:04 GMT  
		Size: 80.2 MB (80156868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbf8bf952bb8dfb4b3d541f4bba137a571525745351c08c5e54cedca086bd5`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.3 MB (1296462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082b3c4f84767770e61ac8e821a5ee44d0e983efbf8b13e4e4aab4d6e3bc9866`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e42467cf2f62990f02e9212aec38ba28e25dca180264cea0a88b2007291aeb9`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b75b5408489e6f25990040f1b8471eb98fa14939ed17dd6ca30fc5ac11717`  
		Last Modified: Sun, 02 Feb 2020 23:15:45 GMT  
		Size: 2.5 MB (2463472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85556fa4b9beeefeb0f9d07cc9838902d1817ee7067626c1d8b92e1ef9e08ad5`  
		Last Modified: Sun, 02 Feb 2020 23:16:09 GMT  
		Size: 61.8 MB (61817813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520906d2d3e8676e38f024b4844415f16350c5b7ef11d97e61cc6f1d6ca39148`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.13` - linux; arm variant v5

```console
$ docker pull redmine@sha256:c94aeafc4839953ffc6f1d091d0be07f4b08b8798aac09ad6d5553bccf4919f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197297445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cd43b3d587718da99aba51d70195446f839e60ec885836249565df5fa1e5f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:53:06 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 02:53:07 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 02:53:07 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 02:53:08 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 03:00:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:00:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:00:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:00:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:00:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:00:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:58:37 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:00:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:00:16 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 10:00:17 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 10:00:18 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 10:00:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 10:00:24 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 10:00:26 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 10:00:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 10:06:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:06:54 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 10:06:55 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 10:06:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 10:06:56 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 10:06:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9d66a1f914bdc48f10a9fb7fa826de1fc4d51127360bfb635de92800427c2c`  
		Last Modified: Sun, 02 Feb 2020 03:18:21 GMT  
		Size: 21.3 MB (21337996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59db49767202ac506ef64e9ad4e78c2222a92d585fc752c47494f69c8d66c40`  
		Last Modified: Sun, 02 Feb 2020 03:18:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb41ba2542818a91d69186164d2baa8245ac6afcfb94f1fcb0d6f6e512d1065`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd4d2b24e257beb61f33391e5e90e9967dc45a757e66afcf682f086ae1db02b`  
		Last Modified: Sun, 02 Feb 2020 10:09:15 GMT  
		Size: 76.0 MB (76036604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774123ad6534a0960d229fc9293ab82687ff0eb673ef39fe99574fdb43fc0300`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 1.3 MB (1254237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba04482a10d8e7ec8a828448873ef5521cb469231897b4757a6e3acb3772cce`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a493edaaf61e6e3d79bca713573cd3eada2ce4a0149ce264e8c82f1a087b407`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943138c7822bb22264d257ee437bf08d764d088aca0a6279ba23f62232241da4`  
		Last Modified: Sun, 02 Feb 2020 10:08:39 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfefd54730a9b78dff4a21cc9482ecaa0526bbced5ccd32add28fead591f587`  
		Last Modified: Sun, 02 Feb 2020 10:08:55 GMT  
		Size: 61.0 MB (61044490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bbf1e5c954dbffe8437807f7327f66456bb1c60539fbea8fd822d16dcdfb2f`  
		Last Modified: Sun, 02 Feb 2020 10:08:37 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.13` - linux; arm variant v7

```console
$ docker pull redmine@sha256:881d1780e71108b5411563601467d378fbb2b121328d6aa9000281f00b52db15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190681440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6968e193bed06b26318c8451aa7afc3c230fbac500a27414d224035a8c7b79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 04:17:15 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 04:17:16 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 04:17:16 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 04:17:17 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 04:23:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 04:23:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 04:23:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 04:23:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 04:23:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 04:23:28 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:35:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:36:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:36:39 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:36:41 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:36:41 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:36:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 18:36:45 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 18:36:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:41:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:41:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:41:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:41:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:41:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:41:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07d29d58da63af2cbe4b2634cbe59f64f36f3e0066cb408f5a2edd98e053034`  
		Last Modified: Sun, 02 Feb 2020 04:40:15 GMT  
		Size: 21.3 MB (21261285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237d4c157ad8e1b0ecbd7678efa8e6b0108df89c7884953e10b971e43222aeea`  
		Last Modified: Sun, 02 Feb 2020 04:40:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0bf238bc883cfcaa3a941ab1b0f83f4ce91332331d703dd4949c2b2261a3c6`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86c1bbd379b656ef6c9d3f742413f0c57faa2904e2a30d715d399a94c70e86b`  
		Last Modified: Sun, 02 Feb 2020 18:43:48 GMT  
		Size: 72.4 MB (72380570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c79ca0fe8317fe54ec51b24b536a24abd0cb9e370ff2dcbdadb1532c3245`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 1.2 MB (1243624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be178bdea130e3af4f2130f197714194a65659e0395e72fdef183eaed592185`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d774b53991a65afa639c84acf0402ff90cab523241a2d3ad7df5645135f3b6dc`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79eb6ad64482bcdea621eba462b32a5f797b655d4c0018be01e8a65048cc0a2a`  
		Last Modified: Sun, 02 Feb 2020 18:43:24 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a37ce0d23a5af8c1f74f177c52941751acca22a5ee59e8072956eb17e572`  
		Last Modified: Sun, 02 Feb 2020 18:43:43 GMT  
		Size: 60.8 MB (60781105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38809f370b0079b82eac7e830b034bf6da09c943e9063536585dfe7c2e78f25`  
		Last Modified: Sun, 02 Feb 2020 18:43:22 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.13` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e8eafd596a79c22008bf82469fa3776b70dedd1179fdd95419314f54a8fc6611
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203238173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a5ded75bfd43a680e9286ad2f2ec09176be76c4f886d02013e7021490e1c40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:36:56 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 10:36:57 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 10:36:57 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 10:36:58 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 10:43:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:43:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:43:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:43:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:43:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:43:43 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:42:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:43:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:43:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:43:50 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:43:51 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:43:52 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:43:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:43:54 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 19:43:54 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 19:43:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:48:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:49:02 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:49:03 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:49:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:49:04 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:49:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ec78c9827c04b80b760ede68bd7175ac30c50c3affbcdb1a54ce990efc340b`  
		Last Modified: Sun, 02 Feb 2020 11:00:05 GMT  
		Size: 21.9 MB (21879217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8ca927e3b9d45908aebe55722c4cd52f0f7dd9bde47c04b8d54aa3724fbb1`  
		Last Modified: Sun, 02 Feb 2020 10:59:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0114a7f90ce24be9c49676ce7650984bc656655cab4d7058d383138ef4bb314d`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb1a386ed4531d7b8ec2c3f5672f9d9c1411be1ad3cf6a95864cb312e89732`  
		Last Modified: Sun, 02 Feb 2020 19:50:53 GMT  
		Size: 78.8 MB (78782615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8578be9b1680f572739cfc6db25ed6501ade895ebc5e30d0634849b0cb238f`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 1.2 MB (1228534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddb3dbc651e684524e1c65ad1e308b834114428efd28784676ed63c9ff7949a`  
		Last Modified: Sun, 02 Feb 2020 19:50:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96574221c0c841bc66a9c26f2ed08aa6e31a742ed05fa152d8f44251abdcbadf`  
		Last Modified: Sun, 02 Feb 2020 19:50:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc4d9969e9404b689c5f8740b9311243bf3407c2c69b2db48df55c84ca7325a`  
		Last Modified: Sun, 02 Feb 2020 19:50:30 GMT  
		Size: 2.5 MB (2463871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb009ed80778f7856c88a80a232596f3e5b9183ff37533f79ac44403c559b12`  
		Last Modified: Sun, 02 Feb 2020 19:50:43 GMT  
		Size: 61.8 MB (61784273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fe2169ada7bbb90d8d5bf5dc65b065e6e36f39d252bacc7005f57301a3fc0f`  
		Last Modified: Sun, 02 Feb 2020 19:50:28 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.13` - linux; 386

```console
$ docker pull redmine@sha256:d86ad9bb76b50667b6d81f9627bd8a34987643c2e20d8214acc4803d54579a00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212835313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaad5817352379ddf843b931d215edab162f606ec5740ef6e4328a30565689f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:22:47 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 10:22:47 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 10:22:48 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 10:22:48 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 10:27:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:28:01 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:22:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:23:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:23:34 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:23:35 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:23:35 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:23:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:23:36 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 13:23:36 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 13:23:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:27:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:27:45 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:27:45 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:27:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:27:46 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:27:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deceb1d6937dd7c5ab8da8ae625647600eaf912e5e42cf7ce805cd7368314bf5`  
		Last Modified: Sun, 02 Feb 2020 10:41:40 GMT  
		Size: 21.5 MB (21545842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43f910fc95479ba6ffe8b02c62974b994bc60e437b10f72d578216b3c934760`  
		Last Modified: Sun, 02 Feb 2020 10:41:36 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672e8d6d4b2a4232841a34d3de7de9005d4a58d98bd7a8ce2e22601d7e026ef`  
		Last Modified: Sun, 02 Feb 2020 13:29:47 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dda6b5b351f4fa6001502299225a2686b84d135fccef81ec3782e4354456a26`  
		Last Modified: Sun, 02 Feb 2020 13:30:21 GMT  
		Size: 81.6 MB (81576493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87417673835a9f2eb395fedbc3789bba85e7957368b9082ad3d7ede0e1be118`  
		Last Modified: Sun, 02 Feb 2020 13:29:47 GMT  
		Size: 1.3 MB (1261019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8eae15c841c71cb6dcd54aae44a8c1de016254e47a3d11fbb37137079b7b00`  
		Last Modified: Sun, 02 Feb 2020 13:29:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973b03ec9c77ef337237646ab70e4bec2b2184bf0f215c3b54753677af78b324`  
		Last Modified: Sun, 02 Feb 2020 13:29:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c370993c1d07a839073931227cae7763db464e4d79b9801e81da36a0a180ae6`  
		Last Modified: Sun, 02 Feb 2020 13:29:48 GMT  
		Size: 2.5 MB (2463471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9fd27bcf3d2044038a7c06fee4626de3f4508af27c329214b69a0806528e6d`  
		Last Modified: Sun, 02 Feb 2020 13:30:04 GMT  
		Size: 61.0 MB (61031067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501022e56770ca5e6c01e546d5079e0da4a0ace3aafe9c926a105d9f008c6f9c`  
		Last Modified: Sun, 02 Feb 2020 13:29:46 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.13` - linux; ppc64le

```console
$ docker pull redmine@sha256:92d2d235dc43a433721f8987c4d9d024bb265748afd2deaee6230f6bad213e04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218599690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734128e8f923729da55c4a99bbbfc57e619a2481ccf170c04667cc85a3b5c376`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:56:58 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:57:05 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:57:08 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:57:12 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 08:04:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 08:04:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 08:04:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 08:04:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 08:05:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 08:05:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:40:07 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:43:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:43:11 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:43:14 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:43:16 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:43:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:43:25 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 16:43:27 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 16:43:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:52:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:52:14 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:52:16 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:52:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:52:20 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:52:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d12304aa6631ac8d42bf1efbf18f76ea3aeff54abba871917165fd259590e6a`  
		Last Modified: Sun, 02 Feb 2020 08:22:34 GMT  
		Size: 22.5 MB (22518893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858322931e6addd835a834cfa5f022232aa257884c1b3b6df9a2f98905b4cd8`  
		Last Modified: Sun, 02 Feb 2020 08:22:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9239b7306ba44ba946d71ae6282bece91bf0792f996cfe99f46ecda2e288b67`  
		Last Modified: Sun, 02 Feb 2020 16:54:00 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f19cd445a9633a3d3fe7d1d3655305e713846023a23ca193cd3fa45e480fcd`  
		Last Modified: Sun, 02 Feb 2020 16:54:18 GMT  
		Size: 86.9 MB (86851603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5496c125aafc5dfc36800a42072774716b1e523b9d96c22824f417264aeba8d8`  
		Last Modified: Sun, 02 Feb 2020 16:53:59 GMT  
		Size: 1.2 MB (1218419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725e9a597dacd2e94b50e226c3b439764c8119cfb6620d6ea048d14d532dab17`  
		Last Modified: Sun, 02 Feb 2020 16:53:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1a18583c13a8b1f51cbaf9f28be0eafd0b3276de46c10c1e7288d4a69ab6d9`  
		Last Modified: Sun, 02 Feb 2020 16:53:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167104d9121defa8cce0b59d169692412b788237a4e9f948b985a5ada11f391`  
		Last Modified: Sun, 02 Feb 2020 16:53:57 GMT  
		Size: 2.5 MB (2463875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c515c0b2c89b7d42b7c7807760beef5c71d04eb4277f3c1a08745feca852f4`  
		Last Modified: Sun, 02 Feb 2020 16:54:09 GMT  
		Size: 62.3 MB (62335852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f37a8e2e2e4693a5d834b1e5a4f8f568608351713b882ebeb076e99eab8bb5`  
		Last Modified: Sun, 02 Feb 2020 16:53:55 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.13` - linux; s390x

```console
$ docker pull redmine@sha256:2370a4642f404adbcdd7c37975e2aa8a4a9c399593cf21b831a7753bf31f1fd2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202577034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889f0b16b19300fc0a24e1c00746a0ab8ffe37e3001f3e859a8832c7e724ffeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:48:48 GMT
ENV RUBY_MAJOR=2.4
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBY_VERSION=2.4.9
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sat, 01 Feb 2020 22:48:49 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sat, 01 Feb 2020 22:51:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:51:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:51:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:51:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:51:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:51:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:31:52 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:32:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:32:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:32:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:32:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:32:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:32:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:32:26 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 03:32:26 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 03:32:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:34:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:34:39 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:34:39 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:34:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:34:39 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:34:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace099387f5254edf276126e046611f26609fd7b03c6eccab25882e8492ab41f`  
		Last Modified: Sat, 01 Feb 2020 22:58:36 GMT  
		Size: 22.2 MB (22151592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b170fa9fa8c788d38c6d6505a94b57d409b33565fd70320c01ce2c1a22977c6`  
		Last Modified: Sat, 01 Feb 2020 22:58:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8b559eb775e7ef2268ad21235635a36ac961841bf8d21ff310f414a71c80e`  
		Last Modified: Sun, 02 Feb 2020 03:36:10 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeaef2a78b559791011534abf0ee2a723b138776372b00019af6f1bcf1b59da`  
		Last Modified: Sun, 02 Feb 2020 03:36:21 GMT  
		Size: 77.9 MB (77940591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf387e3c6ea73ebb6cd13db382724dff9771329e421c8c4ed454fe11927aea0e`  
		Last Modified: Sun, 02 Feb 2020 03:36:09 GMT  
		Size: 1.3 MB (1283198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662f8c8a715db4b4d679682f19697f18f3d11ce144ca00a77c43d87f8251198e`  
		Last Modified: Sun, 02 Feb 2020 03:36:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d75b229dcd884bd3aa4e230e09890af1beccdf1e73b531fdfef09787a956f`  
		Last Modified: Sun, 02 Feb 2020 03:36:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e04af6349cfcff77309336b34350e8fd67956803fe9408f9ff99f121eb6f15`  
		Last Modified: Sun, 02 Feb 2020 03:36:09 GMT  
		Size: 2.5 MB (2463866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babe457f5e43177a09c215741217f93c7a724ca2a67b1bbd2b2ae33bc8e96108`  
		Last Modified: Sun, 02 Feb 2020 03:36:29 GMT  
		Size: 62.2 MB (62231901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9a86c32d5039b929295c3d0162a1177253345f3654fb1e75ddba4477957176`  
		Last Modified: Sun, 02 Feb 2020 03:36:39 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4.13-alpine`

```console
$ docker pull redmine@sha256:8cfd3510d6764d58ce5e117fc1f858d98a5956d836dda57626bc9a9606c7323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.4.13-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:a7fa111e00068a60a15eacaf9ad11ca8db4b7929469cd49f85714a218a76ce56
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156153745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8259090d178e8fb12df9f3d4e431bd79e8270029500b7797ee8cfc1d018a660`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_MAJOR=2.4
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_VERSION=2.4.9
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Thu, 23 Jan 2020 23:00:16 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Thu, 23 Jan 2020 23:06:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 23:06:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 23:06:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 23:06:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 23:06:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 23:06:30 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:24:44 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Fri, 24 Jan 2020 15:24:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Fri, 24 Jan 2020 15:24:53 GMT
ENV RAILS_ENV=production
# Fri, 24 Jan 2020 15:24:53 GMT
WORKDIR /usr/src/redmine
# Fri, 24 Jan 2020 15:24:53 GMT
ENV HOME=/home/redmine
# Fri, 24 Jan 2020 15:24:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 24 Jan 2020 15:24:54 GMT
ENV REDMINE_VERSION=3.4.13
# Fri, 24 Jan 2020 15:24:54 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Fri, 24 Jan 2020 15:24:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:14:36 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:14:36 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:14:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:14:36 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:14:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cfcf9ea42c9ec1b11a4ff2b7d27b908592b82b7e0f30a65325c27366087d9c`  
		Last Modified: Thu, 23 Jan 2020 23:08:27 GMT  
		Size: 22.8 MB (22821242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05133739e27c89886d8326fab4637b17f5be9ba6911377081d055c17802a7cb`  
		Last Modified: Thu, 23 Jan 2020 23:08:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb3b93c12687c41298f346a387962f3814e677aeb84f1b30feb98d66a26c729`  
		Last Modified: Fri, 24 Jan 2020 15:28:15 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b05c8061524c573766c6947d511203084e274f98e5e5139bfc48640f414437c`  
		Last Modified: Fri, 24 Jan 2020 15:28:51 GMT  
		Size: 65.7 MB (65727265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaaf598f37860e727a62490f2f41bc6c1b0ebd0ceea3d847fb6bd37eb3deb8f`  
		Last Modified: Fri, 24 Jan 2020 15:28:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34d3df39933babed2228a5ba0cf7c208dc606e14b42dafb9b1eab9a8f3973c`  
		Last Modified: Fri, 24 Jan 2020 15:28:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c99b56a190ee237d0173d3850c2a76784f7e6171f58eb209d73c0b8a3c6f26`  
		Last Modified: Fri, 24 Jan 2020 15:28:15 GMT  
		Size: 2.5 MB (2464289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0533af3382a728453efbf76861619d015c43eb1005bcb41b3cd9f8380d8b5ff`  
		Last Modified: Sat, 25 Jan 2020 03:17:04 GMT  
		Size: 61.3 MB (61319827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00547284caab370d894d098a856a792d1b5992fbbde4361c5855c222e6999f3b`  
		Last Modified: Sat, 25 Jan 2020 03:16:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4.13-passenger`

```console
$ docker pull redmine@sha256:518f7ba5ab1d7607c7c139ce856a1bc27ea9a4713662f02ab171d0c6568d5f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.4.13-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:99a0b3eae07a19dcc284474670647e4bc3c428177bf660cc450d5eb23eacb794
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232232243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046491c7d289ca8cc45a69e0ec7319dab33637f2086f584788579acfbb30fba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:46:08 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 07:51:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:51:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:51:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:51:35 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:11:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:42 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:11:43 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:11:43 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 23:11:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:04 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:14:04 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:14:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:14:05 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:14:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:14:10 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:14:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:27 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:14:27 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:14:28 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786668394d8864c32001fe2e017691a48e2586962ddadbdd89f3ed1ae3a581b`  
		Last Modified: Sun, 02 Feb 2020 08:05:23 GMT  
		Size: 22.0 MB (22005923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60eeb2d371f01868f9ef2b98cba4e5e4931d7d7f39c22836a1475d47eaa8f79`  
		Last Modified: Sun, 02 Feb 2020 08:05:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0373bcbc7b2dab8ac9a9ba9ece619ebb6ca62092225d55d4d8d78cd9202719`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eca2f7a07b7dea7ab03816feab6eeffd3d7478df839e48b849feea6398c224`  
		Last Modified: Sun, 02 Feb 2020 23:16:04 GMT  
		Size: 80.2 MB (80156868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbf8bf952bb8dfb4b3d541f4bba137a571525745351c08c5e54cedca086bd5`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.3 MB (1296462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082b3c4f84767770e61ac8e821a5ee44d0e983efbf8b13e4e4aab4d6e3bc9866`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e42467cf2f62990f02e9212aec38ba28e25dca180264cea0a88b2007291aeb9`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b75b5408489e6f25990040f1b8471eb98fa14939ed17dd6ca30fc5ac11717`  
		Last Modified: Sun, 02 Feb 2020 23:15:45 GMT  
		Size: 2.5 MB (2463472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85556fa4b9beeefeb0f9d07cc9838902d1817ee7067626c1d8b92e1ef9e08ad5`  
		Last Modified: Sun, 02 Feb 2020 23:16:09 GMT  
		Size: 61.8 MB (61817813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520906d2d3e8676e38f024b4844415f16350c5b7ef11d97e61cc6f1d6ca39148`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74efae5efc3eb3882cd845aa27b0c423d065ffbc50d1f3d7f03e74280c6b47b0`  
		Last Modified: Sun, 02 Feb 2020 23:16:16 GMT  
		Size: 19.9 MB (19937467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b64b2e3c6606664654ed185f8a9485b2eb9639f1228d781cca989f3017d5c9`  
		Last Modified: Sun, 02 Feb 2020 23:16:14 GMT  
		Size: 4.9 MB (4917832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4-alpine`

```console
$ docker pull redmine@sha256:8cfd3510d6764d58ce5e117fc1f858d98a5956d836dda57626bc9a9606c7323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:a7fa111e00068a60a15eacaf9ad11ca8db4b7929469cd49f85714a218a76ce56
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156153745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8259090d178e8fb12df9f3d4e431bd79e8270029500b7797ee8cfc1d018a660`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_MAJOR=2.4
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_VERSION=2.4.9
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Thu, 23 Jan 2020 23:00:16 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Thu, 23 Jan 2020 23:06:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 23:06:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 23:06:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 23:06:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 23:06:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 23:06:30 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:24:44 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Fri, 24 Jan 2020 15:24:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Fri, 24 Jan 2020 15:24:53 GMT
ENV RAILS_ENV=production
# Fri, 24 Jan 2020 15:24:53 GMT
WORKDIR /usr/src/redmine
# Fri, 24 Jan 2020 15:24:53 GMT
ENV HOME=/home/redmine
# Fri, 24 Jan 2020 15:24:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 24 Jan 2020 15:24:54 GMT
ENV REDMINE_VERSION=3.4.13
# Fri, 24 Jan 2020 15:24:54 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Fri, 24 Jan 2020 15:24:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:14:36 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:14:36 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:14:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:14:36 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:14:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cfcf9ea42c9ec1b11a4ff2b7d27b908592b82b7e0f30a65325c27366087d9c`  
		Last Modified: Thu, 23 Jan 2020 23:08:27 GMT  
		Size: 22.8 MB (22821242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05133739e27c89886d8326fab4637b17f5be9ba6911377081d055c17802a7cb`  
		Last Modified: Thu, 23 Jan 2020 23:08:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb3b93c12687c41298f346a387962f3814e677aeb84f1b30feb98d66a26c729`  
		Last Modified: Fri, 24 Jan 2020 15:28:15 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b05c8061524c573766c6947d511203084e274f98e5e5139bfc48640f414437c`  
		Last Modified: Fri, 24 Jan 2020 15:28:51 GMT  
		Size: 65.7 MB (65727265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaaf598f37860e727a62490f2f41bc6c1b0ebd0ceea3d847fb6bd37eb3deb8f`  
		Last Modified: Fri, 24 Jan 2020 15:28:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34d3df39933babed2228a5ba0cf7c208dc606e14b42dafb9b1eab9a8f3973c`  
		Last Modified: Fri, 24 Jan 2020 15:28:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c99b56a190ee237d0173d3850c2a76784f7e6171f58eb209d73c0b8a3c6f26`  
		Last Modified: Fri, 24 Jan 2020 15:28:15 GMT  
		Size: 2.5 MB (2464289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0533af3382a728453efbf76861619d015c43eb1005bcb41b3cd9f8380d8b5ff`  
		Last Modified: Sat, 25 Jan 2020 03:17:04 GMT  
		Size: 61.3 MB (61319827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00547284caab370d894d098a856a792d1b5992fbbde4361c5855c222e6999f3b`  
		Last Modified: Sat, 25 Jan 2020 03:16:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4-passenger`

```console
$ docker pull redmine@sha256:518f7ba5ab1d7607c7c139ce856a1bc27ea9a4713662f02ab171d0c6568d5f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:99a0b3eae07a19dcc284474670647e4bc3c428177bf660cc450d5eb23eacb794
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232232243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046491c7d289ca8cc45a69e0ec7319dab33637f2086f584788579acfbb30fba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:46:08 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 07:51:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:51:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:51:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:51:35 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:11:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:42 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:11:43 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:11:43 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 23:11:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:04 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:14:04 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:14:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:14:05 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:14:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:14:10 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:14:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:27 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:14:27 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:14:28 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786668394d8864c32001fe2e017691a48e2586962ddadbdd89f3ed1ae3a581b`  
		Last Modified: Sun, 02 Feb 2020 08:05:23 GMT  
		Size: 22.0 MB (22005923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60eeb2d371f01868f9ef2b98cba4e5e4931d7d7f39c22836a1475d47eaa8f79`  
		Last Modified: Sun, 02 Feb 2020 08:05:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0373bcbc7b2dab8ac9a9ba9ece619ebb6ca62092225d55d4d8d78cd9202719`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eca2f7a07b7dea7ab03816feab6eeffd3d7478df839e48b849feea6398c224`  
		Last Modified: Sun, 02 Feb 2020 23:16:04 GMT  
		Size: 80.2 MB (80156868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbf8bf952bb8dfb4b3d541f4bba137a571525745351c08c5e54cedca086bd5`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.3 MB (1296462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082b3c4f84767770e61ac8e821a5ee44d0e983efbf8b13e4e4aab4d6e3bc9866`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e42467cf2f62990f02e9212aec38ba28e25dca180264cea0a88b2007291aeb9`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b75b5408489e6f25990040f1b8471eb98fa14939ed17dd6ca30fc5ac11717`  
		Last Modified: Sun, 02 Feb 2020 23:15:45 GMT  
		Size: 2.5 MB (2463472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85556fa4b9beeefeb0f9d07cc9838902d1817ee7067626c1d8b92e1ef9e08ad5`  
		Last Modified: Sun, 02 Feb 2020 23:16:09 GMT  
		Size: 61.8 MB (61817813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520906d2d3e8676e38f024b4844415f16350c5b7ef11d97e61cc6f1d6ca39148`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74efae5efc3eb3882cd845aa27b0c423d065ffbc50d1f3d7f03e74280c6b47b0`  
		Last Modified: Sun, 02 Feb 2020 23:16:16 GMT  
		Size: 19.9 MB (19937467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b64b2e3c6606664654ed185f8a9485b2eb9639f1228d781cca989f3017d5c9`  
		Last Modified: Sun, 02 Feb 2020 23:16:14 GMT  
		Size: 4.9 MB (4917832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3-alpine`

```console
$ docker pull redmine@sha256:8cfd3510d6764d58ce5e117fc1f858d98a5956d836dda57626bc9a9606c7323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:a7fa111e00068a60a15eacaf9ad11ca8db4b7929469cd49f85714a218a76ce56
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156153745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8259090d178e8fb12df9f3d4e431bd79e8270029500b7797ee8cfc1d018a660`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_MAJOR=2.4
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_VERSION=2.4.9
# Thu, 23 Jan 2020 23:00:15 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Thu, 23 Jan 2020 23:00:16 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Thu, 23 Jan 2020 23:06:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 23:06:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 23:06:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 23:06:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 23:06:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 23:06:30 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:24:44 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Fri, 24 Jan 2020 15:24:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Fri, 24 Jan 2020 15:24:53 GMT
ENV RAILS_ENV=production
# Fri, 24 Jan 2020 15:24:53 GMT
WORKDIR /usr/src/redmine
# Fri, 24 Jan 2020 15:24:53 GMT
ENV HOME=/home/redmine
# Fri, 24 Jan 2020 15:24:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 24 Jan 2020 15:24:54 GMT
ENV REDMINE_VERSION=3.4.13
# Fri, 24 Jan 2020 15:24:54 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Fri, 24 Jan 2020 15:24:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:14:36 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:14:36 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:14:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:14:36 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:14:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cfcf9ea42c9ec1b11a4ff2b7d27b908592b82b7e0f30a65325c27366087d9c`  
		Last Modified: Thu, 23 Jan 2020 23:08:27 GMT  
		Size: 22.8 MB (22821242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05133739e27c89886d8326fab4637b17f5be9ba6911377081d055c17802a7cb`  
		Last Modified: Thu, 23 Jan 2020 23:08:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb3b93c12687c41298f346a387962f3814e677aeb84f1b30feb98d66a26c729`  
		Last Modified: Fri, 24 Jan 2020 15:28:15 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b05c8061524c573766c6947d511203084e274f98e5e5139bfc48640f414437c`  
		Last Modified: Fri, 24 Jan 2020 15:28:51 GMT  
		Size: 65.7 MB (65727265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaaf598f37860e727a62490f2f41bc6c1b0ebd0ceea3d847fb6bd37eb3deb8f`  
		Last Modified: Fri, 24 Jan 2020 15:28:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34d3df39933babed2228a5ba0cf7c208dc606e14b42dafb9b1eab9a8f3973c`  
		Last Modified: Fri, 24 Jan 2020 15:28:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c99b56a190ee237d0173d3850c2a76784f7e6171f58eb209d73c0b8a3c6f26`  
		Last Modified: Fri, 24 Jan 2020 15:28:15 GMT  
		Size: 2.5 MB (2464289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0533af3382a728453efbf76861619d015c43eb1005bcb41b3cd9f8380d8b5ff`  
		Last Modified: Sat, 25 Jan 2020 03:17:04 GMT  
		Size: 61.3 MB (61319827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00547284caab370d894d098a856a792d1b5992fbbde4361c5855c222e6999f3b`  
		Last Modified: Sat, 25 Jan 2020 03:16:56 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3-passenger`

```console
$ docker pull redmine@sha256:518f7ba5ab1d7607c7c139ce856a1bc27ea9a4713662f02ab171d0c6568d5f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:99a0b3eae07a19dcc284474670647e4bc3c428177bf660cc450d5eb23eacb794
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232232243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046491c7d289ca8cc45a69e0ec7319dab33637f2086f584788579acfbb30fba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:46:08 GMT
ENV RUBY_MAJOR=2.4
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_VERSION=2.4.9
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBY_DOWNLOAD_SHA256=0c4e000253ef7187feeb940a01a1c7594f28d63aa16f978e892a0e2864f58614
# Sun, 02 Feb 2020 07:46:09 GMT
ENV RUBYGEMS_VERSION=3.0.3
# Sun, 02 Feb 2020 07:51:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	ruby -e 'exit(Gem::Version.create(ENV["RUBYGEMS_VERSION"]) > Gem::Version.create(Gem::VERSION))'; 	gem update --system "$RUBYGEMS_VERSION" && rm -r /root/.gem/; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:51:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:51:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:51:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:51:35 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:11:11 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:42 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:11:43 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:11:43 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:11:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_VERSION=3.4.13
# Sun, 02 Feb 2020 23:11:44 GMT
ENV REDMINE_DOWNLOAD_MD5=5f17b35dfe73118067f63fb535332cfb
# Sun, 02 Feb 2020 23:11:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:04 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:14:04 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:14:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:14:05 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:14:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:14:10 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:14:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:14:27 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:14:27 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:14:28 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7786668394d8864c32001fe2e017691a48e2586962ddadbdd89f3ed1ae3a581b`  
		Last Modified: Sun, 02 Feb 2020 08:05:23 GMT  
		Size: 22.0 MB (22005923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60eeb2d371f01868f9ef2b98cba4e5e4931d7d7f39c22836a1475d47eaa8f79`  
		Last Modified: Sun, 02 Feb 2020 08:05:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0373bcbc7b2dab8ac9a9ba9ece619ebb6ca62092225d55d4d8d78cd9202719`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eca2f7a07b7dea7ab03816feab6eeffd3d7478df839e48b849feea6398c224`  
		Last Modified: Sun, 02 Feb 2020 23:16:04 GMT  
		Size: 80.2 MB (80156868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbf8bf952bb8dfb4b3d541f4bba137a571525745351c08c5e54cedca086bd5`  
		Last Modified: Sun, 02 Feb 2020 23:15:46 GMT  
		Size: 1.3 MB (1296462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082b3c4f84767770e61ac8e821a5ee44d0e983efbf8b13e4e4aab4d6e3bc9866`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e42467cf2f62990f02e9212aec38ba28e25dca180264cea0a88b2007291aeb9`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435b75b5408489e6f25990040f1b8471eb98fa14939ed17dd6ca30fc5ac11717`  
		Last Modified: Sun, 02 Feb 2020 23:15:45 GMT  
		Size: 2.5 MB (2463472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85556fa4b9beeefeb0f9d07cc9838902d1817ee7067626c1d8b92e1ef9e08ad5`  
		Last Modified: Sun, 02 Feb 2020 23:16:09 GMT  
		Size: 61.8 MB (61817813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520906d2d3e8676e38f024b4844415f16350c5b7ef11d97e61cc6f1d6ca39148`  
		Last Modified: Sun, 02 Feb 2020 23:15:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74efae5efc3eb3882cd845aa27b0c423d065ffbc50d1f3d7f03e74280c6b47b0`  
		Last Modified: Sun, 02 Feb 2020 23:16:16 GMT  
		Size: 19.9 MB (19937467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b64b2e3c6606664654ed185f8a9485b2eb9639f1228d781cca989f3017d5c9`  
		Last Modified: Sun, 02 Feb 2020 23:16:14 GMT  
		Size: 4.9 MB (4917832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4`

```console
$ docker pull redmine@sha256:2b80a2f231e0c3151048b900e06e2f1188e6c48a6d67fa57666498d6d3e11d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4` - linux; amd64

```console
$ docker pull redmine@sha256:41c835c5d62a566e3205ec0de8b69a0d7ba82ab92db3f2c6f6f694079a39ce7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215447934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd730be099a4d92ac9ece41b026c8a9eeb9bbce1391737a3b27a2a7a5c96fb10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:d81487b3c1ad872dcf937922c70e1b33aa56ba4ce5190286fa2d86d8adeedc35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204856480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb08d7d0f07498236e41fdcf83db177fea39c1c452b01cf798acd1a6878621b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:16:09 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 02:16:12 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 02:16:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 02:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 02:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 02:19:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 02:20:03 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:44:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:46:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:46:22 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 09:46:22 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 09:46:23 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 09:46:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 09:46:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 09:46:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 09:46:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 09:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:50:23 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 09:50:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 09:50:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 09:50:25 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 09:50:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdd05ffdd7888092a6ef03be377963c297edec0344ce762bb6b3e1e2f114b94`  
		Last Modified: Sun, 02 Feb 2020 03:16:40 GMT  
		Size: 20.7 MB (20712712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e99c39d252f8cf22fae4749b2764aec83374848c63b8546989494f7f7a1cd2`  
		Last Modified: Sun, 02 Feb 2020 03:16:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff532b6c7852f386bab467c7b3f4b83b928ea314de236796805380d538c9717`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2386bd4b4f50f1d8f93b32303170d0866887841332213e58a371ca1bb7a20589`  
		Last Modified: Sun, 02 Feb 2020 10:07:52 GMT  
		Size: 88.7 MB (88656018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3116bbee905e3f17958856da579a4d33255abeddc081a9673f7e7751b098ebe`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.3 MB (1265374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a450151953d1dd4bd9521617998e60400bbde5af211dc4477b78be4b3f12675b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98603c054417f4f97943b58f87a4064bff0a6fdcc842f801c987da619b29ff3b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23326958468d4e64c292656ee80e58902c0ffdb4d9dd0ebe0f3ab5264ce8d22`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 2.7 MB (2735847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb53308614fca2cb01c7b7851bffaab106d45dee36ec93f25b881241ff56a0`  
		Last Modified: Sun, 02 Feb 2020 10:07:31 GMT  
		Size: 56.3 MB (56326279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2affc3b6a6c7eac6ca68be7e12a92c5998344deee6abc0a859b5698bb25dfdcc`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:9e0f94008f8a2c500a8c924488a7529a4a1c3ec8ed88647c3dccdb05eb336cfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20602d68bea242b9e0df73f8c1cb3ec695ca48e7b2d34ca2193d1e41d38a76d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 03:44:54 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 03:44:55 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 03:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 03:49:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:49:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:49:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:49:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:23:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:24:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:24:56 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:24:57 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:24:57 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:25:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 18:25:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:28:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:28:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:28:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:28:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:28:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:28:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fb6d3f67479293696c0ab1862f3d3cc1ccc4c655c60fe8a6b96d3958a13be`  
		Last Modified: Sun, 02 Feb 2020 04:38:21 GMT  
		Size: 20.6 MB (20620356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b57ca0c1f7b3cf1cf1382ec1048a03d8dd1fdd32b795c902f5305133d27c78`  
		Last Modified: Sun, 02 Feb 2020 04:38:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7e084272859dee62cdf07109bf3e8805638cf379acc552cbe57103d7127d7`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acdfe876f23507df2a4699b62233e5db893da68e0714670b2969ef99c3e4a85`  
		Last Modified: Sun, 02 Feb 2020 18:42:40 GMT  
		Size: 84.7 MB (84707975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4870f608fea5ec1df650afdeb0c7cac2ba24338f4ed4869ec1edf65dc3fa0c10`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.3 MB (1258130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cc28beecc94c51bb3c2e9bba9085acdb45f0cf6597ddba6286a4bc6244615`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0de6c18a6248274446744a98c3073bd3b138523d0975cc79e90fd546a2347`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1f3d8cad218ec457642439ef0e21e35b559965647074943fc07db7dafb8743`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 2.7 MB (2735837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcaa8a3e3e84f31845a917fd61aad8eb9520cc340d01f508f4506549341c5b4`  
		Last Modified: Sun, 02 Feb 2020 18:42:22 GMT  
		Size: 56.1 MB (56088174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b64e249084f0b4a1d8e939df4443bff48c435a17efb9d45dbc395d6444a984`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:46f7558e68186926a79a1f9eefe59f70dabee4e16f3e1bd4ef81f04306c34965
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211195925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31550a4fb8bf9ac5cca4bef14798e52e08b79e17ed4b36c9836b2c07eb42992`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 10:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 10:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:09:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:09:34 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:31:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:32:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:32:45 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:32:46 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:32:46 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:32:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:32:48 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 19:32:49 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 19:32:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:36:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:36:05 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:36:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:36:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:36:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:36:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e033592aeac21c0ce386b8333f16f6235250b4a12589032d45952f28aae99`  
		Last Modified: Sun, 02 Feb 2020 10:58:31 GMT  
		Size: 21.3 MB (21281648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb4967683b60ada551e77eafdd485daad99a6f1942cf491c5976877e6a7ca01`  
		Last Modified: Sun, 02 Feb 2020 10:58:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1923f0191bb3e7f14a51e3b4eeeb28deece511d37ce6f497c40bda83f1465`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154e1dcb614be456b08a22da421f1470ea51295943e88b2a0eada860e5585180`  
		Last Modified: Sun, 02 Feb 2020 19:49:49 GMT  
		Size: 91.6 MB (91645303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6070fa62d6076ace9b5fdbbc4425f553159ca73742af8b61b21c7cc62e28dc5b`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.2 MB (1242753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9b86ab04e3610da622ab684cf5116bb375dc072d2904d889e41ad6446aa3a9`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6d1aea2f7bdeae18fdbd703e35ea9ccadf83021960b2e8910c5c9a409e4d31`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade23107ce3d3cfd24a6e9442e7c716423ce08ab6e9554e2a3a54deb2cdca4f`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 2.7 MB (2735843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31458ee540982d7eea52baa93517c1a913991aac9330899a1fdf3bc869f11d`  
		Last Modified: Sun, 02 Feb 2020 19:49:33 GMT  
		Size: 57.2 MB (57190715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac7f8eecf6e47209978b8484171c538983fd231a5a833b0b3a7d4e8975d3411`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; 386

```console
$ docker pull redmine@sha256:0fb7c16c6ed2458c52ade08fcc7aee843a838ef7d90da9d98d4b4501a83fdd28
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220910454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69331927d39ab8ede3ae82a7009bdd1d19a8f90f6aa5e7807c4387dbcacd51a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 09:52:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 09:52:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 09:52:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 09:52:15 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:14:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:15:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:15:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:15:23 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:15:24 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:15:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:15:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 13:15:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 13:15:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:17:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:17:59 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:17:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:18:00 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:18:00 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e5d604e111de701bacf8c6952c8658d23d38b32c40a699c9ffdd0a50c9f45`  
		Last Modified: Sun, 02 Feb 2020 10:40:28 GMT  
		Size: 20.9 MB (20885510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640ed0b4362227a298cdba0f568b4516440d1041650eed93add06c421dec473`  
		Last Modified: Sun, 02 Feb 2020 10:40:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ba87587e473025c53ccdc291f0ff3cb00d050037298dbbf09bea4e9a96e273`  
		Last Modified: Sun, 02 Feb 2020 13:28:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d1e5b965a8e946b00d9e203d026eebcea799c872e86aab10892b19a25573e1`  
		Last Modified: Sun, 02 Feb 2020 13:28:53 GMT  
		Size: 94.7 MB (94691964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7823a2f443dfa05bc739245b9e6562ed6ce736eab799b6ab47ced9d157ec68`  
		Last Modified: Sun, 02 Feb 2020 13:28:07 GMT  
		Size: 1.3 MB (1275381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5977e8eed0d5080afd68d86e283b526522639b7d238c53aa3c350446da6e0496`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8464fc08c66d5812b90b3ec3186df531b6e99fb17df90d61454d428340e781d2`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4688da52009d0f4d4436d254808e6b9dcd304a95222fa3ac1611d00225809182`  
		Last Modified: Sun, 02 Feb 2020 13:28:08 GMT  
		Size: 2.7 MB (2735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f56b39600309d764a728a6af38afc43b71852287e8236e74ca5eac034a1c5`  
		Last Modified: Sun, 02 Feb 2020 13:28:28 GMT  
		Size: 56.4 MB (56364790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09d36e70af01f3cd70a01df4e6d5949d56fe641d8d895fcc242c91f75451e4e`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; ppc64le

```console
$ docker pull redmine@sha256:65f7bee1e807535980a5d3a2a6faf187e1f706da092dc09b923e4b11b041f930
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227251848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceee0df6cf0aa3c88905cdf9aba7438a919d629c7e66e784521ef17b3204d2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:21:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:24:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:24:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:24:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:24:26 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:24:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:24:34 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 16:24:36 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 16:24:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:28:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:28:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:28:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:28:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:28:27 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:28:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da40f6ba93d0a415759b121cffd59a714d0f9c8ea1c9ae9399dfd8ee2ba0a49c`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba55cb767e55fbec8edc12b9b116d3fd5959e82478ad073aa4c16b21ed5fe9`  
		Last Modified: Sun, 02 Feb 2020 16:53:06 GMT  
		Size: 100.3 MB (100283339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aac9fe590c395f90d840a0b6f490cb158a13321b799e4994a1bd1514d25eef`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.2 MB (1232443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97021c4ffbeff7d0d7e315631e4eb080205367e8997876c04d80d02271b6e38`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207503016878e07ef9be87106c3f4a0b46ad75c6f65c9ac0bc9c33ab6af9f34a`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e246ddcfdcc8d1ac853928cfed7c2d2e591666b1afe656a637c3b1ea14e7e7e`  
		Last Modified: Sun, 02 Feb 2020 16:52:40 GMT  
		Size: 2.7 MB (2735859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac7132221ca2c54eae8b8ee34564de1198fe84a573e709c1c589cf6d02cca5`  
		Last Modified: Sun, 02 Feb 2020 16:52:48 GMT  
		Size: 57.8 MB (57820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5915d8cf49b43d9212479a3fa1d53b6f44892c808bddf15679344b9ba445851`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; s390x

```console
$ docker pull redmine@sha256:ab1568d6b226e18d614f69224ab5082f76ab6c3c459575b451c0b43a044e4c88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210607230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e81bbd4d53db9fe58b1f99028cbe990f74848ac4052582c07576953e60742dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_MAJOR=2.6
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_VERSION=2.6.5
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sat, 01 Feb 2020 22:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:36:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:36:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:36:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:24:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:25:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:25:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:25:35 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:25:36 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 03:25:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:28:15 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:28:15 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:28:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:28:16 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:28:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f50ba1593f8ab66d1deaf12e190c35ecfea96815beda37efe10f1246f342b`  
		Last Modified: Sat, 01 Feb 2020 22:57:18 GMT  
		Size: 21.6 MB (21592569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a5d1fd225888733445fbc5a03464b232ab7c659a3bf619e93c5670a0ca594`  
		Last Modified: Sat, 01 Feb 2020 22:57:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6b52758f305e2a6eca340f3801ffcd699d9f9863ebfe870573fbea05f125b`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b9c2d954e677f77134627d444d4526d3dd757e20731a3db791ee045bd3ff5`  
		Last Modified: Sun, 02 Feb 2020 03:35:13 GMT  
		Size: 90.8 MB (90810821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4b03bbe680823684e8167d23322040275fc82bb40b38251bd1aca1d9759997`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.3 MB (1297549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a56833da980d550b03c0656e63d42b60190fa8f5b743d0efd1679e03cb5ea`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6743cd35c07b27ae19792d6c94243798a11247fa7a5f0fd8d63ec5fec7f8c8`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0844cdbf926f537d20bc1295376495cb2b126746d549e3cc88402e855e2f92`  
		Last Modified: Sun, 02 Feb 2020 03:34:58 GMT  
		Size: 2.7 MB (2735858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0c8052dd4f2d2e8e61136ca875e5667f9fdd869156f21339a352533be465b`  
		Last Modified: Sun, 02 Feb 2020 03:35:25 GMT  
		Size: 57.7 MB (57664549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b47a626d921e859c5def90095c9624aa612e063bcacdce5bb5485574308e28`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0`

```console
$ docker pull redmine@sha256:51cf0db3ce2e52f8e38bda7e35de802a32698dcfaa21d472418a7f6f339c1765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.0` - linux; amd64

```console
$ docker pull redmine@sha256:1fb12e419b0a49b1e1152dd0a49a1229081eab9749fdfebefe013172fd21136a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0536b9aa56fcaca5b842f10e4da1a8692d7452f07314cef23a504c42be2e0888`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:08:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:08:14 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:08:15 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:08:15 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:08:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 23:08:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:10:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:10:36 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:10:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:10:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:10:37 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:10:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e4294239b93a415547d7ab07efd905c97e6d5cd38367a3809a649494cf7db`  
		Last Modified: Sun, 02 Feb 2020 23:15:32 GMT  
		Size: 80.2 MB (80157093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2f9a930414120fefaf4321e07d9bc8dcbd8ec7ca9ba05c520dc67d0e4ff03a`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 1.3 MB (1296494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2f9bb8ae42a98cef0b2b70af2d5d9b47d6693b66311c5dd6095df3461d8ed`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3270569fdb3ae3e25e0b216001776a9ce6aa85a7bcc5acb18260f2fdb30c1c`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d83bd5a7bd3769713978c809fc2ed4ac6a5d3f2af7efd9a640632bac698181`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 2.5 MB (2534075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8a1fdb3b50ff2c1653f433baf8f68562eee2ecfb4ffbf5f9afd2bbd1d6520`  
		Last Modified: Sun, 02 Feb 2020 23:15:26 GMT  
		Size: 60.9 MB (60907215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8709fc44e86af6f0b1852704d044e7d3acdaa51d3740f17de450b837a2842ada`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v5

```console
$ docker pull redmine@sha256:6c2dea6b181f65d669cd93ed3528823ad6e7c0c2140ff489ea485ad4339bc3b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195708230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca154e81c746b1401a3a68110b0600c1c2948a0bcbf4064ca3ccf6d17f645b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:16:09 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 02:16:12 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 02:16:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 02:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 02:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 02:19:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 02:20:03 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:44:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:52:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:52:01 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 09:52:02 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 09:52:02 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 09:52:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 09:52:05 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 09:52:06 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 09:52:10 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 09:58:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:58:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 09:58:22 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 09:58:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 09:58:25 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 09:58:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdd05ffdd7888092a6ef03be377963c297edec0344ce762bb6b3e1e2f114b94`  
		Last Modified: Sun, 02 Feb 2020 03:16:40 GMT  
		Size: 20.7 MB (20712712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e99c39d252f8cf22fae4749b2764aec83374848c63b8546989494f7f7a1cd2`  
		Last Modified: Sun, 02 Feb 2020 03:16:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff532b6c7852f386bab467c7b3f4b83b928ea314de236796805380d538c9717`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0debc39d343e6e3774b7272d41bc3baba5a731a248e516631a84c1a159f8e92`  
		Last Modified: Sun, 02 Feb 2020 10:08:31 GMT  
		Size: 76.0 MB (76036784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad080b035428964df5b926dd10100e90e780aba975a158a431d3981e83c258b8`  
		Last Modified: Sun, 02 Feb 2020 10:08:04 GMT  
		Size: 1.3 MB (1254160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9727bc7a8173e4995f60fae2c0648c1cb27901cb17032ad9158742d2802b6515`  
		Last Modified: Sun, 02 Feb 2020 10:08:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd97e49c236fbff5f8e9ddea74499d2220bd7243c51337af425617f8a7dd7ae`  
		Last Modified: Sun, 02 Feb 2020 10:08:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea72640d58690c2a87f00a90e7227a898f083e23da7c935365625fed397ce753`  
		Last Modified: Sun, 02 Feb 2020 10:08:03 GMT  
		Size: 2.5 MB (2534555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7020374fdf35ade6f5496677da7317db93a9a3e8c281ee32fecbbc5655f43a1`  
		Last Modified: Sun, 02 Feb 2020 10:08:20 GMT  
		Size: 60.0 MB (60009770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bf767d92dd343de578ca08df993171a406b4a73d327094036a50f3bcb4d694`  
		Last Modified: Sun, 02 Feb 2020 10:08:01 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v7

```console
$ docker pull redmine@sha256:4dbd87580980509cbbf9eb2faed3487dd838c70b0a340cc5d34cc26cd93a0697
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189070588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a5a9fffea811d8af6fa54b83fb1330aa1bcef75233e87d0d8c3d088924485d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 03:44:54 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 03:44:55 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 03:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 03:49:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:49:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:49:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:49:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:23:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:30:04 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:30:05 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:30:06 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:30:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:30:08 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 18:30:09 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 18:30:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:35:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:35:05 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:35:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:35:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:35:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:35:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fb6d3f67479293696c0ab1862f3d3cc1ccc4c655c60fe8a6b96d3958a13be`  
		Last Modified: Sun, 02 Feb 2020 04:38:21 GMT  
		Size: 20.6 MB (20620356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b57ca0c1f7b3cf1cf1382ec1048a03d8dd1fdd32b795c902f5305133d27c78`  
		Last Modified: Sun, 02 Feb 2020 04:38:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7e084272859dee62cdf07109bf3e8805638cf379acc552cbe57103d7127d7`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e104fe9485a65cb7009689247a7f3279307ab06a65dfdd07ba8290063ef633d`  
		Last Modified: Sun, 02 Feb 2020 18:43:15 GMT  
		Size: 72.4 MB (72380711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f645750290023c9d579ce5d8d229a217e752ee31223f7ebbfeddca7d09fee7`  
		Last Modified: Sun, 02 Feb 2020 18:42:52 GMT  
		Size: 1.2 MB (1243635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3da3e342093b034808871b1fcfd96ce4b27042b649ed5d5fca856c7f760030`  
		Last Modified: Sun, 02 Feb 2020 18:42:50 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea1722626d95bb5e6a8440660811353b350de7cf9ed6ad332f28167758102c`  
		Last Modified: Sun, 02 Feb 2020 18:42:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dfd22f0655a0078f989bf86c8e2d4de810eb655bd53cd272025d4272d1f52b`  
		Last Modified: Sun, 02 Feb 2020 18:42:52 GMT  
		Size: 2.5 MB (2534552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f580129dad45e99f273f53cce072ed626b74908cf25ad2b4005771ff2da35d`  
		Last Modified: Sun, 02 Feb 2020 18:43:05 GMT  
		Size: 59.7 MB (59740346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7386bc5064d24d7af27c0dba7b9f473e157d36c6a528843fb108382b4693c12`  
		Last Modified: Sun, 02 Feb 2020 18:42:50 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:31d0a2e1303e6a2f616d7a65093a4cce14c235ddbe60d4f2323d247810b32255
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201745561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afe3671dcb2427c4a9ebffe1256b94800fabf4aa3c811db07badf1d619460f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 10:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 10:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:09:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:09:34 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:31:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:37:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:37:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:37:26 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:37:27 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:37:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:37:29 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 19:37:29 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 19:37:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:42:18 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:42:18 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:42:20 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:42:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e033592aeac21c0ce386b8333f16f6235250b4a12589032d45952f28aae99`  
		Last Modified: Sun, 02 Feb 2020 10:58:31 GMT  
		Size: 21.3 MB (21281648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb4967683b60ada551e77eafdd485daad99a6f1942cf491c5976877e6a7ca01`  
		Last Modified: Sun, 02 Feb 2020 10:58:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1923f0191bb3e7f14a51e3b4eeeb28deece511d37ce6f497c40bda83f1465`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5f14dc9abac2c100831fb7ea178877ff05163e88c62ef508cec6b31a2c27b3`  
		Last Modified: Sun, 02 Feb 2020 19:50:23 GMT  
		Size: 78.8 MB (78782389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff22765dfede87ffc01c66dc4a1ff6e51b5e2285c60ca2e87ec617b423f34810`  
		Last Modified: Sun, 02 Feb 2020 19:50:00 GMT  
		Size: 1.2 MB (1228523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266472f711cc95a6ac2fceecb8d1c8c122aa225aa5e8cc1f95fe1a7afd28425e`  
		Last Modified: Sun, 02 Feb 2020 19:49:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c8bd20143f04bb99f19283e36e282b820eec5ecca096a04792ee11940a69fd`  
		Last Modified: Sun, 02 Feb 2020 19:49:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba00daac1502b9597e8c1b7fa358980e0d15859a882afa1efeb72adfb031d18`  
		Last Modified: Sun, 02 Feb 2020 19:50:00 GMT  
		Size: 2.5 MB (2534551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fd2a7971de77afd3bf9dac0d28f2feaaaa1d71f4459911de4eaa820f6863e5`  
		Last Modified: Sun, 02 Feb 2020 19:50:13 GMT  
		Size: 60.8 MB (60818786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0759dc6098727952a71eb529a6018228beabaceaaa4f3f55c03af6003211b05c`  
		Last Modified: Sun, 02 Feb 2020 19:49:58 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; 386

```console
$ docker pull redmine@sha256:cd40ab2fc80db046a6c772691186250784802f66e7637e1357eaba546e1bf8c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211227496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb22387bb7fef33c7038f98059e4fcee47e650be02bbf6b3766559024cbda79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 09:52:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 09:52:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 09:52:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 09:52:15 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:14:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:18:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:18:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:18:54 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:18:55 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:18:55 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:18:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:18:57 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 13:18:57 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 13:19:02 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:22:44 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:22:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:22:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:22:44 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:22:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e5d604e111de701bacf8c6952c8658d23d38b32c40a699c9ffdd0a50c9f45`  
		Last Modified: Sun, 02 Feb 2020 10:40:28 GMT  
		Size: 20.9 MB (20885510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640ed0b4362227a298cdba0f568b4516440d1041650eed93add06c421dec473`  
		Last Modified: Sun, 02 Feb 2020 10:40:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ba87587e473025c53ccdc291f0ff3cb00d050037298dbbf09bea4e9a96e273`  
		Last Modified: Sun, 02 Feb 2020 13:28:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23285f5e4fd2211e5dd83b3d9abbd88c4893cb1fcc0c95b2fdf82e742ad536b6`  
		Last Modified: Sun, 02 Feb 2020 13:29:41 GMT  
		Size: 81.6 MB (81578008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4ba44b54d575e33cd561c5576f18f737b67b90647005b03e07e515bba197ba`  
		Last Modified: Sun, 02 Feb 2020 13:29:02 GMT  
		Size: 1.3 MB (1261070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465519f608e773081043b8bc5a2b46c01c2894deaa8bfb86eb3b257800624f31`  
		Last Modified: Sun, 02 Feb 2020 13:29:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f7561cadbea7812f06b25b6616435e71bd286964b72d636fe082c2136f82d2`  
		Last Modified: Sun, 02 Feb 2020 13:29:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ad2eef3938496a97d9adb80612e05c1c71c16ad4a23829edbc8e6dccd580bc`  
		Last Modified: Sun, 02 Feb 2020 13:29:03 GMT  
		Size: 2.5 MB (2534060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae55b277d9cc63ceb3d330dfb42c30ea4d81d4b12f16346625353788ee8062a1`  
		Last Modified: Sun, 02 Feb 2020 13:29:24 GMT  
		Size: 60.0 MB (60011426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5871f31b53779bce80d02336aba94c299796374dc70bb5125b06d8467fcfadd2`  
		Last Modified: Sun, 02 Feb 2020 13:29:00 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; ppc64le

```console
$ docker pull redmine@sha256:99f6e4184a5177e4a36c341711649085b215540f8e8a2ef609dbfce38706bf5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217310777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83644c3b6e368e5e89295c3aec950b2bdfdbc29ddde65e54b63c7eaab85e7f19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:21:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:30:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:31:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:31:45 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:31:49 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:31:51 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:31:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:32:02 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 16:32:07 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 16:32:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:39:35 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:39:37 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:39:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:39:47 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:39:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da40f6ba93d0a415759b121cffd59a714d0f9c8ea1c9ae9399dfd8ee2ba0a49c`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261ee6fd2a6d9d42650b58c3cb253fbf1dfc2803b7226f4d0bbe9513b6ca7875`  
		Last Modified: Sun, 02 Feb 2020 16:53:45 GMT  
		Size: 86.9 MB (86851602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37353a6719ea4dbeea63efec3d3bbde975c78db30b20e21d784fe53390254ec9`  
		Last Modified: Sun, 02 Feb 2020 16:53:27 GMT  
		Size: 1.2 MB (1218441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba77378b9a6a3e7ec0d936055f219696ce33843d2c24d1eeb7eb83eb61015c2`  
		Last Modified: Sun, 02 Feb 2020 16:53:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c086b3188f726d4fb87b4bce0797b9b6f418ffc093fc57f5caaa9d0ef5f256`  
		Last Modified: Sun, 02 Feb 2020 16:53:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ce50def134e25b25a9920c34e1247472b5073666d373977520883be5e7d958`  
		Last Modified: Sun, 02 Feb 2020 16:53:24 GMT  
		Size: 2.5 MB (2534557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09fa4288c4052fc8c135d7f40d557b135de7d11b8d0b1aa11077c1cfabe8a6a`  
		Last Modified: Sun, 02 Feb 2020 16:53:33 GMT  
		Size: 61.5 MB (61526447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4ee651837f6c230e484ba208ff00ecce6ad5984385c1d31ba17adfa04ce11e`  
		Last Modified: Sun, 02 Feb 2020 16:53:23 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; s390x

```console
$ docker pull redmine@sha256:cbf070b34f864e9c96515dfa45421eaa20238ef10162705f9822d124da8cd1f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201200831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b645759a5ba2c2f260e05766ef5dcd1734dcf2951d74bed1cbaa1bab9997ff66`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_MAJOR=2.6
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_VERSION=2.6.5
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sat, 01 Feb 2020 22:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:36:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:36:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:36:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:24:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:29:08 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:29:08 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:29:08 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:29:09 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 03:29:09 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 03:29:12 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:31:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:31:46 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:31:47 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:31:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:31:47 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:31:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f50ba1593f8ab66d1deaf12e190c35ecfea96815beda37efe10f1246f342b`  
		Last Modified: Sat, 01 Feb 2020 22:57:18 GMT  
		Size: 21.6 MB (21592569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a5d1fd225888733445fbc5a03464b232ab7c659a3bf619e93c5670a0ca594`  
		Last Modified: Sat, 01 Feb 2020 22:57:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6b52758f305e2a6eca340f3801ffcd699d9f9863ebfe870573fbea05f125b`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1fac4ff5cafcd8c72e5f5c2b0ad9b65c0da0b68abc477c04f5a694df30d7c3`  
		Last Modified: Sun, 02 Feb 2020 03:35:46 GMT  
		Size: 77.9 MB (77938026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff38b0dcb3bbc5f2f4a3d6db1ff6ae6e4fec958a96bed443120d073beeb3cca`  
		Last Modified: Sun, 02 Feb 2020 03:35:34 GMT  
		Size: 1.3 MB (1283142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfc8a9f51c523c1393ad678485fc7c27af0973daadb7a4b898403c00a470c1c`  
		Last Modified: Sun, 02 Feb 2020 03:35:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48652af6bf6cc23d74f44d8dac9310630f1e54ce1970a50e76b9b08e969d36e3`  
		Last Modified: Sun, 02 Feb 2020 03:35:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e7113be31cd9d1c3b63a00e3042d6f6990a6f7abfd9153a63665f70c0f57f6`  
		Last Modified: Sun, 02 Feb 2020 03:35:48 GMT  
		Size: 2.5 MB (2534555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1af23fc8a237407ee124dbcb2eb6f80a2c91d2a5940c439c678cdfef1dbd90`  
		Last Modified: Sun, 02 Feb 2020 03:35:39 GMT  
		Size: 61.3 MB (61346659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d58b291fa3d29f6414a4697d6ff544204e41efc77488f71a129e007e9c1f0`  
		Last Modified: Sun, 02 Feb 2020 03:36:03 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.6`

```console
$ docker pull redmine@sha256:51cf0db3ce2e52f8e38bda7e35de802a32698dcfaa21d472418a7f6f339c1765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.0.6` - linux; amd64

```console
$ docker pull redmine@sha256:1fb12e419b0a49b1e1152dd0a49a1229081eab9749fdfebefe013172fd21136a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0536b9aa56fcaca5b842f10e4da1a8692d7452f07314cef23a504c42be2e0888`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:08:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:08:14 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:08:15 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:08:15 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:08:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 23:08:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:10:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:10:36 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:10:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:10:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:10:37 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:10:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e4294239b93a415547d7ab07efd905c97e6d5cd38367a3809a649494cf7db`  
		Last Modified: Sun, 02 Feb 2020 23:15:32 GMT  
		Size: 80.2 MB (80157093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2f9a930414120fefaf4321e07d9bc8dcbd8ec7ca9ba05c520dc67d0e4ff03a`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 1.3 MB (1296494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2f9bb8ae42a98cef0b2b70af2d5d9b47d6693b66311c5dd6095df3461d8ed`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3270569fdb3ae3e25e0b216001776a9ce6aa85a7bcc5acb18260f2fdb30c1c`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d83bd5a7bd3769713978c809fc2ed4ac6a5d3f2af7efd9a640632bac698181`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 2.5 MB (2534075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8a1fdb3b50ff2c1653f433baf8f68562eee2ecfb4ffbf5f9afd2bbd1d6520`  
		Last Modified: Sun, 02 Feb 2020 23:15:26 GMT  
		Size: 60.9 MB (60907215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8709fc44e86af6f0b1852704d044e7d3acdaa51d3740f17de450b837a2842ada`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.6` - linux; arm variant v5

```console
$ docker pull redmine@sha256:6c2dea6b181f65d669cd93ed3528823ad6e7c0c2140ff489ea485ad4339bc3b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195708230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca154e81c746b1401a3a68110b0600c1c2948a0bcbf4064ca3ccf6d17f645b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:16:09 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 02:16:12 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 02:16:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 02:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 02:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 02:19:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 02:20:03 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:44:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:52:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:52:01 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 09:52:02 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 09:52:02 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 09:52:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 09:52:05 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 09:52:06 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 09:52:10 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 09:58:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:58:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 09:58:22 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 09:58:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 09:58:25 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 09:58:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdd05ffdd7888092a6ef03be377963c297edec0344ce762bb6b3e1e2f114b94`  
		Last Modified: Sun, 02 Feb 2020 03:16:40 GMT  
		Size: 20.7 MB (20712712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e99c39d252f8cf22fae4749b2764aec83374848c63b8546989494f7f7a1cd2`  
		Last Modified: Sun, 02 Feb 2020 03:16:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff532b6c7852f386bab467c7b3f4b83b928ea314de236796805380d538c9717`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0debc39d343e6e3774b7272d41bc3baba5a731a248e516631a84c1a159f8e92`  
		Last Modified: Sun, 02 Feb 2020 10:08:31 GMT  
		Size: 76.0 MB (76036784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad080b035428964df5b926dd10100e90e780aba975a158a431d3981e83c258b8`  
		Last Modified: Sun, 02 Feb 2020 10:08:04 GMT  
		Size: 1.3 MB (1254160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9727bc7a8173e4995f60fae2c0648c1cb27901cb17032ad9158742d2802b6515`  
		Last Modified: Sun, 02 Feb 2020 10:08:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd97e49c236fbff5f8e9ddea74499d2220bd7243c51337af425617f8a7dd7ae`  
		Last Modified: Sun, 02 Feb 2020 10:08:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea72640d58690c2a87f00a90e7227a898f083e23da7c935365625fed397ce753`  
		Last Modified: Sun, 02 Feb 2020 10:08:03 GMT  
		Size: 2.5 MB (2534555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7020374fdf35ade6f5496677da7317db93a9a3e8c281ee32fecbbc5655f43a1`  
		Last Modified: Sun, 02 Feb 2020 10:08:20 GMT  
		Size: 60.0 MB (60009770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bf767d92dd343de578ca08df993171a406b4a73d327094036a50f3bcb4d694`  
		Last Modified: Sun, 02 Feb 2020 10:08:01 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.6` - linux; arm variant v7

```console
$ docker pull redmine@sha256:4dbd87580980509cbbf9eb2faed3487dd838c70b0a340cc5d34cc26cd93a0697
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189070588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a5a9fffea811d8af6fa54b83fb1330aa1bcef75233e87d0d8c3d088924485d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 03:44:54 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 03:44:55 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 03:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 03:49:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:49:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:49:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:49:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:23:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:30:04 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:30:05 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:30:06 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:30:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:30:08 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 18:30:09 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 18:30:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:35:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:35:05 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:35:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:35:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:35:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:35:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fb6d3f67479293696c0ab1862f3d3cc1ccc4c655c60fe8a6b96d3958a13be`  
		Last Modified: Sun, 02 Feb 2020 04:38:21 GMT  
		Size: 20.6 MB (20620356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b57ca0c1f7b3cf1cf1382ec1048a03d8dd1fdd32b795c902f5305133d27c78`  
		Last Modified: Sun, 02 Feb 2020 04:38:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7e084272859dee62cdf07109bf3e8805638cf379acc552cbe57103d7127d7`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e104fe9485a65cb7009689247a7f3279307ab06a65dfdd07ba8290063ef633d`  
		Last Modified: Sun, 02 Feb 2020 18:43:15 GMT  
		Size: 72.4 MB (72380711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f645750290023c9d579ce5d8d229a217e752ee31223f7ebbfeddca7d09fee7`  
		Last Modified: Sun, 02 Feb 2020 18:42:52 GMT  
		Size: 1.2 MB (1243635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3da3e342093b034808871b1fcfd96ce4b27042b649ed5d5fca856c7f760030`  
		Last Modified: Sun, 02 Feb 2020 18:42:50 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea1722626d95bb5e6a8440660811353b350de7cf9ed6ad332f28167758102c`  
		Last Modified: Sun, 02 Feb 2020 18:42:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dfd22f0655a0078f989bf86c8e2d4de810eb655bd53cd272025d4272d1f52b`  
		Last Modified: Sun, 02 Feb 2020 18:42:52 GMT  
		Size: 2.5 MB (2534552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f580129dad45e99f273f53cce072ed626b74908cf25ad2b4005771ff2da35d`  
		Last Modified: Sun, 02 Feb 2020 18:43:05 GMT  
		Size: 59.7 MB (59740346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7386bc5064d24d7af27c0dba7b9f473e157d36c6a528843fb108382b4693c12`  
		Last Modified: Sun, 02 Feb 2020 18:42:50 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.6` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:31d0a2e1303e6a2f616d7a65093a4cce14c235ddbe60d4f2323d247810b32255
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201745561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afe3671dcb2427c4a9ebffe1256b94800fabf4aa3c811db07badf1d619460f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 10:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 10:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:09:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:09:34 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:31:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:37:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:37:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:37:26 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:37:27 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:37:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:37:29 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 19:37:29 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 19:37:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:42:18 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:42:18 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:42:20 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:42:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e033592aeac21c0ce386b8333f16f6235250b4a12589032d45952f28aae99`  
		Last Modified: Sun, 02 Feb 2020 10:58:31 GMT  
		Size: 21.3 MB (21281648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb4967683b60ada551e77eafdd485daad99a6f1942cf491c5976877e6a7ca01`  
		Last Modified: Sun, 02 Feb 2020 10:58:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1923f0191bb3e7f14a51e3b4eeeb28deece511d37ce6f497c40bda83f1465`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5f14dc9abac2c100831fb7ea178877ff05163e88c62ef508cec6b31a2c27b3`  
		Last Modified: Sun, 02 Feb 2020 19:50:23 GMT  
		Size: 78.8 MB (78782389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff22765dfede87ffc01c66dc4a1ff6e51b5e2285c60ca2e87ec617b423f34810`  
		Last Modified: Sun, 02 Feb 2020 19:50:00 GMT  
		Size: 1.2 MB (1228523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266472f711cc95a6ac2fceecb8d1c8c122aa225aa5e8cc1f95fe1a7afd28425e`  
		Last Modified: Sun, 02 Feb 2020 19:49:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c8bd20143f04bb99f19283e36e282b820eec5ecca096a04792ee11940a69fd`  
		Last Modified: Sun, 02 Feb 2020 19:49:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba00daac1502b9597e8c1b7fa358980e0d15859a882afa1efeb72adfb031d18`  
		Last Modified: Sun, 02 Feb 2020 19:50:00 GMT  
		Size: 2.5 MB (2534551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fd2a7971de77afd3bf9dac0d28f2feaaaa1d71f4459911de4eaa820f6863e5`  
		Last Modified: Sun, 02 Feb 2020 19:50:13 GMT  
		Size: 60.8 MB (60818786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0759dc6098727952a71eb529a6018228beabaceaaa4f3f55c03af6003211b05c`  
		Last Modified: Sun, 02 Feb 2020 19:49:58 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.6` - linux; 386

```console
$ docker pull redmine@sha256:cd40ab2fc80db046a6c772691186250784802f66e7637e1357eaba546e1bf8c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211227496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb22387bb7fef33c7038f98059e4fcee47e650be02bbf6b3766559024cbda79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 09:52:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 09:52:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 09:52:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 09:52:15 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:14:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:18:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:18:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:18:54 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:18:55 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:18:55 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:18:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:18:57 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 13:18:57 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 13:19:02 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:22:44 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:22:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:22:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:22:44 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:22:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e5d604e111de701bacf8c6952c8658d23d38b32c40a699c9ffdd0a50c9f45`  
		Last Modified: Sun, 02 Feb 2020 10:40:28 GMT  
		Size: 20.9 MB (20885510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640ed0b4362227a298cdba0f568b4516440d1041650eed93add06c421dec473`  
		Last Modified: Sun, 02 Feb 2020 10:40:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ba87587e473025c53ccdc291f0ff3cb00d050037298dbbf09bea4e9a96e273`  
		Last Modified: Sun, 02 Feb 2020 13:28:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23285f5e4fd2211e5dd83b3d9abbd88c4893cb1fcc0c95b2fdf82e742ad536b6`  
		Last Modified: Sun, 02 Feb 2020 13:29:41 GMT  
		Size: 81.6 MB (81578008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4ba44b54d575e33cd561c5576f18f737b67b90647005b03e07e515bba197ba`  
		Last Modified: Sun, 02 Feb 2020 13:29:02 GMT  
		Size: 1.3 MB (1261070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465519f608e773081043b8bc5a2b46c01c2894deaa8bfb86eb3b257800624f31`  
		Last Modified: Sun, 02 Feb 2020 13:29:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f7561cadbea7812f06b25b6616435e71bd286964b72d636fe082c2136f82d2`  
		Last Modified: Sun, 02 Feb 2020 13:29:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ad2eef3938496a97d9adb80612e05c1c71c16ad4a23829edbc8e6dccd580bc`  
		Last Modified: Sun, 02 Feb 2020 13:29:03 GMT  
		Size: 2.5 MB (2534060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae55b277d9cc63ceb3d330dfb42c30ea4d81d4b12f16346625353788ee8062a1`  
		Last Modified: Sun, 02 Feb 2020 13:29:24 GMT  
		Size: 60.0 MB (60011426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5871f31b53779bce80d02336aba94c299796374dc70bb5125b06d8467fcfadd2`  
		Last Modified: Sun, 02 Feb 2020 13:29:00 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.6` - linux; ppc64le

```console
$ docker pull redmine@sha256:99f6e4184a5177e4a36c341711649085b215540f8e8a2ef609dbfce38706bf5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217310777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83644c3b6e368e5e89295c3aec950b2bdfdbc29ddde65e54b63c7eaab85e7f19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:21:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:30:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:31:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:31:45 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:31:49 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:31:51 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:31:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:32:02 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 16:32:07 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 16:32:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:39:35 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:39:37 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:39:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:39:47 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:39:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da40f6ba93d0a415759b121cffd59a714d0f9c8ea1c9ae9399dfd8ee2ba0a49c`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261ee6fd2a6d9d42650b58c3cb253fbf1dfc2803b7226f4d0bbe9513b6ca7875`  
		Last Modified: Sun, 02 Feb 2020 16:53:45 GMT  
		Size: 86.9 MB (86851602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37353a6719ea4dbeea63efec3d3bbde975c78db30b20e21d784fe53390254ec9`  
		Last Modified: Sun, 02 Feb 2020 16:53:27 GMT  
		Size: 1.2 MB (1218441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba77378b9a6a3e7ec0d936055f219696ce33843d2c24d1eeb7eb83eb61015c2`  
		Last Modified: Sun, 02 Feb 2020 16:53:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c086b3188f726d4fb87b4bce0797b9b6f418ffc093fc57f5caaa9d0ef5f256`  
		Last Modified: Sun, 02 Feb 2020 16:53:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ce50def134e25b25a9920c34e1247472b5073666d373977520883be5e7d958`  
		Last Modified: Sun, 02 Feb 2020 16:53:24 GMT  
		Size: 2.5 MB (2534557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09fa4288c4052fc8c135d7f40d557b135de7d11b8d0b1aa11077c1cfabe8a6a`  
		Last Modified: Sun, 02 Feb 2020 16:53:33 GMT  
		Size: 61.5 MB (61526447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4ee651837f6c230e484ba208ff00ecce6ad5984385c1d31ba17adfa04ce11e`  
		Last Modified: Sun, 02 Feb 2020 16:53:23 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.6` - linux; s390x

```console
$ docker pull redmine@sha256:cbf070b34f864e9c96515dfa45421eaa20238ef10162705f9822d124da8cd1f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201200831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b645759a5ba2c2f260e05766ef5dcd1734dcf2951d74bed1cbaa1bab9997ff66`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_MAJOR=2.6
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_VERSION=2.6.5
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sat, 01 Feb 2020 22:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:36:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:36:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:36:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:24:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:29:08 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:29:08 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:29:08 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:29:09 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 03:29:09 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 03:29:12 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:31:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:31:46 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:31:47 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:31:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:31:47 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:31:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f50ba1593f8ab66d1deaf12e190c35ecfea96815beda37efe10f1246f342b`  
		Last Modified: Sat, 01 Feb 2020 22:57:18 GMT  
		Size: 21.6 MB (21592569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a5d1fd225888733445fbc5a03464b232ab7c659a3bf619e93c5670a0ca594`  
		Last Modified: Sat, 01 Feb 2020 22:57:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6b52758f305e2a6eca340f3801ffcd699d9f9863ebfe870573fbea05f125b`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1fac4ff5cafcd8c72e5f5c2b0ad9b65c0da0b68abc477c04f5a694df30d7c3`  
		Last Modified: Sun, 02 Feb 2020 03:35:46 GMT  
		Size: 77.9 MB (77938026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff38b0dcb3bbc5f2f4a3d6db1ff6ae6e4fec958a96bed443120d073beeb3cca`  
		Last Modified: Sun, 02 Feb 2020 03:35:34 GMT  
		Size: 1.3 MB (1283142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfc8a9f51c523c1393ad678485fc7c27af0973daadb7a4b898403c00a470c1c`  
		Last Modified: Sun, 02 Feb 2020 03:35:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48652af6bf6cc23d74f44d8dac9310630f1e54ce1970a50e76b9b08e969d36e3`  
		Last Modified: Sun, 02 Feb 2020 03:35:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e7113be31cd9d1c3b63a00e3042d6f6990a6f7abfd9153a63665f70c0f57f6`  
		Last Modified: Sun, 02 Feb 2020 03:35:48 GMT  
		Size: 2.5 MB (2534555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1af23fc8a237407ee124dbcb2eb6f80a2c91d2a5940c439c678cdfef1dbd90`  
		Last Modified: Sun, 02 Feb 2020 03:35:39 GMT  
		Size: 61.3 MB (61346659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d58b291fa3d29f6414a4697d6ff544204e41efc77488f71a129e007e9c1f0`  
		Last Modified: Sun, 02 Feb 2020 03:36:03 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.6-alpine`

```console
$ docker pull redmine@sha256:a979e29cbfde5de17798d4e9b91d5a2a77bc84a9b9c3f4e4835b7c963166cff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0.6-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:8f90d09cf079ff5be64d694722794ab5df0c046e03fffa3af8c832bb6cbf8245
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154087478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdba488d0c766cd6832878ee15e5c07d7b7d5df81f499df81bcf689c2e9cf4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_VERSION=2.6.5
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Thu, 23 Jan 2020 22:54:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:55:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 22:55:00 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:20:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Fri, 24 Jan 2020 15:20:41 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Fri, 24 Jan 2020 15:20:41 GMT
ENV RAILS_ENV=production
# Fri, 24 Jan 2020 15:20:42 GMT
WORKDIR /usr/src/redmine
# Fri, 24 Jan 2020 15:20:42 GMT
ENV HOME=/home/redmine
# Fri, 24 Jan 2020 15:20:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 24 Jan 2020 15:22:38 GMT
ENV REDMINE_VERSION=4.0.6
# Fri, 24 Jan 2020 15:22:38 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Fri, 24 Jan 2020 15:22:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:09:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:09:32 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:09:32 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:09:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:09:32 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:09:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058dc40fe23d25b2a6b8b9a31a6064c2eac5b373f52d5acb6d9219394f18a6c`  
		Last Modified: Thu, 23 Jan 2020 23:08:01 GMT  
		Size: 22.1 MB (22078401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabe7657d0e85ffedf267cb47d1b5a01f8da1f182f429defe848b0cdb2233ab1`  
		Last Modified: Thu, 23 Jan 2020 23:07:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a8cf67746eef043d81238dcc09e82c7404ac11ded1b543a0d44ef4b43b1f6f`  
		Last Modified: Fri, 24 Jan 2020 15:26:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec375945f2a0726e842b7cbcd0e44f464791dd670c87ba5c94886a64624e61f7`  
		Last Modified: Fri, 24 Jan 2020 15:27:14 GMT  
		Size: 65.7 MB (65727287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fc0e569dec0c9540830c542087692271d164dda41eb6fd4236c8214f080eb2`  
		Last Modified: Fri, 24 Jan 2020 15:26:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ae2ddcba63d2890fcefdbbd31d9646ee5e5428bb2c37578422be8f60b9363f`  
		Last Modified: Fri, 24 Jan 2020 15:26:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5298d654e31d6672b6f7171281f78f6536b027b9dc7e209b2d0f3589d8cbda2`  
		Last Modified: Fri, 24 Jan 2020 15:27:23 GMT  
		Size: 2.5 MB (2535813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841e92874997bbd5b01af23711a5d3dfc55accce652163e641d73a8647f36be7`  
		Last Modified: Sat, 25 Jan 2020 03:16:29 GMT  
		Size: 59.9 MB (59924857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2825ca0d048103b819a2f778649e5c4592cfc7f7030da727b2249617a19b0b0`  
		Last Modified: Sat, 25 Jan 2020 03:16:20 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.6-passenger`

```console
$ docker pull redmine@sha256:d157730f9bf80c9369b8bdfd63f18ea91a6cfc487405d2e2a3ce20f94af4639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0.6-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:3ab9cb06beb588c63d2086cd2e549753bc133761ca9a67165c8fac8af1d0c9e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230834815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b821a9ea9521ede181b3494f0b4a453e7379403f9058304e6fec576e7329f698`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:08:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:08:14 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:08:15 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:08:15 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:08:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 23:08:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:10:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:10:36 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:10:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:10:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:10:37 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:10:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:10:43 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:10:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:00 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:11:00 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:11:01 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e4294239b93a415547d7ab07efd905c97e6d5cd38367a3809a649494cf7db`  
		Last Modified: Sun, 02 Feb 2020 23:15:32 GMT  
		Size: 80.2 MB (80157093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2f9a930414120fefaf4321e07d9bc8dcbd8ec7ca9ba05c520dc67d0e4ff03a`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 1.3 MB (1296494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2f9bb8ae42a98cef0b2b70af2d5d9b47d6693b66311c5dd6095df3461d8ed`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3270569fdb3ae3e25e0b216001776a9ce6aa85a7bcc5acb18260f2fdb30c1c`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d83bd5a7bd3769713978c809fc2ed4ac6a5d3f2af7efd9a640632bac698181`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 2.5 MB (2534075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8a1fdb3b50ff2c1653f433baf8f68562eee2ecfb4ffbf5f9afd2bbd1d6520`  
		Last Modified: Sun, 02 Feb 2020 23:15:26 GMT  
		Size: 60.9 MB (60907215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8709fc44e86af6f0b1852704d044e7d3acdaa51d3740f17de450b837a2842ada`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20438b02e458ba69c6544ee458cdf2cfbd9cf1c558ccaac6ad5a90f6bc5904e0`  
		Last Modified: Sun, 02 Feb 2020 23:15:40 GMT  
		Size: 19.9 MB (19939914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f440cb2c1c2286c3ff784ee9253249180f0ed1872c1a64b58b681d2d2e291031`  
		Last Modified: Sun, 02 Feb 2020 23:15:38 GMT  
		Size: 4.9 MB (4917837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-alpine`

```console
$ docker pull redmine@sha256:a979e29cbfde5de17798d4e9b91d5a2a77bc84a9b9c3f4e4835b7c963166cff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:8f90d09cf079ff5be64d694722794ab5df0c046e03fffa3af8c832bb6cbf8245
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154087478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdba488d0c766cd6832878ee15e5c07d7b7d5df81f499df81bcf689c2e9cf4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_VERSION=2.6.5
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Thu, 23 Jan 2020 22:54:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:55:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 22:55:00 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:20:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Fri, 24 Jan 2020 15:20:41 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Fri, 24 Jan 2020 15:20:41 GMT
ENV RAILS_ENV=production
# Fri, 24 Jan 2020 15:20:42 GMT
WORKDIR /usr/src/redmine
# Fri, 24 Jan 2020 15:20:42 GMT
ENV HOME=/home/redmine
# Fri, 24 Jan 2020 15:20:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 24 Jan 2020 15:22:38 GMT
ENV REDMINE_VERSION=4.0.6
# Fri, 24 Jan 2020 15:22:38 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Fri, 24 Jan 2020 15:22:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:09:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:09:32 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:09:32 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:09:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:09:32 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:09:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058dc40fe23d25b2a6b8b9a31a6064c2eac5b373f52d5acb6d9219394f18a6c`  
		Last Modified: Thu, 23 Jan 2020 23:08:01 GMT  
		Size: 22.1 MB (22078401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabe7657d0e85ffedf267cb47d1b5a01f8da1f182f429defe848b0cdb2233ab1`  
		Last Modified: Thu, 23 Jan 2020 23:07:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a8cf67746eef043d81238dcc09e82c7404ac11ded1b543a0d44ef4b43b1f6f`  
		Last Modified: Fri, 24 Jan 2020 15:26:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec375945f2a0726e842b7cbcd0e44f464791dd670c87ba5c94886a64624e61f7`  
		Last Modified: Fri, 24 Jan 2020 15:27:14 GMT  
		Size: 65.7 MB (65727287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fc0e569dec0c9540830c542087692271d164dda41eb6fd4236c8214f080eb2`  
		Last Modified: Fri, 24 Jan 2020 15:26:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ae2ddcba63d2890fcefdbbd31d9646ee5e5428bb2c37578422be8f60b9363f`  
		Last Modified: Fri, 24 Jan 2020 15:26:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5298d654e31d6672b6f7171281f78f6536b027b9dc7e209b2d0f3589d8cbda2`  
		Last Modified: Fri, 24 Jan 2020 15:27:23 GMT  
		Size: 2.5 MB (2535813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841e92874997bbd5b01af23711a5d3dfc55accce652163e641d73a8647f36be7`  
		Last Modified: Sat, 25 Jan 2020 03:16:29 GMT  
		Size: 59.9 MB (59924857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2825ca0d048103b819a2f778649e5c4592cfc7f7030da727b2249617a19b0b0`  
		Last Modified: Sat, 25 Jan 2020 03:16:20 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-passenger`

```console
$ docker pull redmine@sha256:d157730f9bf80c9369b8bdfd63f18ea91a6cfc487405d2e2a3ce20f94af4639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.0-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:3ab9cb06beb588c63d2086cd2e549753bc133761ca9a67165c8fac8af1d0c9e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230834815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b821a9ea9521ede181b3494f0b4a453e7379403f9058304e6fec576e7329f698`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:08:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:08:14 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:08:15 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:08:15 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:08:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_VERSION=4.0.6
# Sun, 02 Feb 2020 23:08:16 GMT
ENV REDMINE_DOWNLOAD_MD5=897bfcaa4a49539b10d0529ce103f919
# Sun, 02 Feb 2020 23:08:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:10:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:10:36 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:10:36 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:10:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:10:37 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:10:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:10:43 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:10:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:11:00 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:11:00 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:11:01 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e4294239b93a415547d7ab07efd905c97e6d5cd38367a3809a649494cf7db`  
		Last Modified: Sun, 02 Feb 2020 23:15:32 GMT  
		Size: 80.2 MB (80157093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2f9a930414120fefaf4321e07d9bc8dcbd8ec7ca9ba05c520dc67d0e4ff03a`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 1.3 MB (1296494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2f9bb8ae42a98cef0b2b70af2d5d9b47d6693b66311c5dd6095df3461d8ed`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3270569fdb3ae3e25e0b216001776a9ce6aa85a7bcc5acb18260f2fdb30c1c`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d83bd5a7bd3769713978c809fc2ed4ac6a5d3f2af7efd9a640632bac698181`  
		Last Modified: Sun, 02 Feb 2020 23:15:17 GMT  
		Size: 2.5 MB (2534075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8a1fdb3b50ff2c1653f433baf8f68562eee2ecfb4ffbf5f9afd2bbd1d6520`  
		Last Modified: Sun, 02 Feb 2020 23:15:26 GMT  
		Size: 60.9 MB (60907215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8709fc44e86af6f0b1852704d044e7d3acdaa51d3740f17de450b837a2842ada`  
		Last Modified: Sun, 02 Feb 2020 23:15:16 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20438b02e458ba69c6544ee458cdf2cfbd9cf1c558ccaac6ad5a90f6bc5904e0`  
		Last Modified: Sun, 02 Feb 2020 23:15:40 GMT  
		Size: 19.9 MB (19939914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f440cb2c1c2286c3ff784ee9253249180f0ed1872c1a64b58b681d2d2e291031`  
		Last Modified: Sun, 02 Feb 2020 23:15:38 GMT  
		Size: 4.9 MB (4917837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1`

```console
$ docker pull redmine@sha256:2b80a2f231e0c3151048b900e06e2f1188e6c48a6d67fa57666498d6d3e11d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.1` - linux; amd64

```console
$ docker pull redmine@sha256:41c835c5d62a566e3205ec0de8b69a0d7ba82ab92db3f2c6f6f694079a39ce7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215447934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd730be099a4d92ac9ece41b026c8a9eeb9bbce1391737a3b27a2a7a5c96fb10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v5

```console
$ docker pull redmine@sha256:d81487b3c1ad872dcf937922c70e1b33aa56ba4ce5190286fa2d86d8adeedc35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204856480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb08d7d0f07498236e41fdcf83db177fea39c1c452b01cf798acd1a6878621b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:16:09 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 02:16:12 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 02:16:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 02:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 02:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 02:19:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 02:20:03 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:44:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:46:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:46:22 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 09:46:22 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 09:46:23 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 09:46:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 09:46:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 09:46:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 09:46:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 09:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:50:23 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 09:50:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 09:50:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 09:50:25 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 09:50:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdd05ffdd7888092a6ef03be377963c297edec0344ce762bb6b3e1e2f114b94`  
		Last Modified: Sun, 02 Feb 2020 03:16:40 GMT  
		Size: 20.7 MB (20712712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e99c39d252f8cf22fae4749b2764aec83374848c63b8546989494f7f7a1cd2`  
		Last Modified: Sun, 02 Feb 2020 03:16:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff532b6c7852f386bab467c7b3f4b83b928ea314de236796805380d538c9717`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2386bd4b4f50f1d8f93b32303170d0866887841332213e58a371ca1bb7a20589`  
		Last Modified: Sun, 02 Feb 2020 10:07:52 GMT  
		Size: 88.7 MB (88656018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3116bbee905e3f17958856da579a4d33255abeddc081a9673f7e7751b098ebe`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.3 MB (1265374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a450151953d1dd4bd9521617998e60400bbde5af211dc4477b78be4b3f12675b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98603c054417f4f97943b58f87a4064bff0a6fdcc842f801c987da619b29ff3b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23326958468d4e64c292656ee80e58902c0ffdb4d9dd0ebe0f3ab5264ce8d22`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 2.7 MB (2735847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb53308614fca2cb01c7b7851bffaab106d45dee36ec93f25b881241ff56a0`  
		Last Modified: Sun, 02 Feb 2020 10:07:31 GMT  
		Size: 56.3 MB (56326279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2affc3b6a6c7eac6ca68be7e12a92c5998344deee6abc0a859b5698bb25dfdcc`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v7

```console
$ docker pull redmine@sha256:9e0f94008f8a2c500a8c924488a7529a4a1c3ec8ed88647c3dccdb05eb336cfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20602d68bea242b9e0df73f8c1cb3ec695ca48e7b2d34ca2193d1e41d38a76d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 03:44:54 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 03:44:55 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 03:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 03:49:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:49:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:49:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:49:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:23:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:24:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:24:56 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:24:57 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:24:57 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:25:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 18:25:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:28:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:28:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:28:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:28:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:28:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:28:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fb6d3f67479293696c0ab1862f3d3cc1ccc4c655c60fe8a6b96d3958a13be`  
		Last Modified: Sun, 02 Feb 2020 04:38:21 GMT  
		Size: 20.6 MB (20620356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b57ca0c1f7b3cf1cf1382ec1048a03d8dd1fdd32b795c902f5305133d27c78`  
		Last Modified: Sun, 02 Feb 2020 04:38:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7e084272859dee62cdf07109bf3e8805638cf379acc552cbe57103d7127d7`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acdfe876f23507df2a4699b62233e5db893da68e0714670b2969ef99c3e4a85`  
		Last Modified: Sun, 02 Feb 2020 18:42:40 GMT  
		Size: 84.7 MB (84707975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4870f608fea5ec1df650afdeb0c7cac2ba24338f4ed4869ec1edf65dc3fa0c10`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.3 MB (1258130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cc28beecc94c51bb3c2e9bba9085acdb45f0cf6597ddba6286a4bc6244615`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0de6c18a6248274446744a98c3073bd3b138523d0975cc79e90fd546a2347`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1f3d8cad218ec457642439ef0e21e35b559965647074943fc07db7dafb8743`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 2.7 MB (2735837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcaa8a3e3e84f31845a917fd61aad8eb9520cc340d01f508f4506549341c5b4`  
		Last Modified: Sun, 02 Feb 2020 18:42:22 GMT  
		Size: 56.1 MB (56088174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b64e249084f0b4a1d8e939df4443bff48c435a17efb9d45dbc395d6444a984`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:46f7558e68186926a79a1f9eefe59f70dabee4e16f3e1bd4ef81f04306c34965
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211195925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31550a4fb8bf9ac5cca4bef14798e52e08b79e17ed4b36c9836b2c07eb42992`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 10:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 10:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:09:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:09:34 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:31:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:32:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:32:45 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:32:46 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:32:46 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:32:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:32:48 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 19:32:49 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 19:32:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:36:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:36:05 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:36:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:36:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:36:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:36:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e033592aeac21c0ce386b8333f16f6235250b4a12589032d45952f28aae99`  
		Last Modified: Sun, 02 Feb 2020 10:58:31 GMT  
		Size: 21.3 MB (21281648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb4967683b60ada551e77eafdd485daad99a6f1942cf491c5976877e6a7ca01`  
		Last Modified: Sun, 02 Feb 2020 10:58:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1923f0191bb3e7f14a51e3b4eeeb28deece511d37ce6f497c40bda83f1465`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154e1dcb614be456b08a22da421f1470ea51295943e88b2a0eada860e5585180`  
		Last Modified: Sun, 02 Feb 2020 19:49:49 GMT  
		Size: 91.6 MB (91645303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6070fa62d6076ace9b5fdbbc4425f553159ca73742af8b61b21c7cc62e28dc5b`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.2 MB (1242753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9b86ab04e3610da622ab684cf5116bb375dc072d2904d889e41ad6446aa3a9`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6d1aea2f7bdeae18fdbd703e35ea9ccadf83021960b2e8910c5c9a409e4d31`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade23107ce3d3cfd24a6e9442e7c716423ce08ab6e9554e2a3a54deb2cdca4f`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 2.7 MB (2735843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31458ee540982d7eea52baa93517c1a913991aac9330899a1fdf3bc869f11d`  
		Last Modified: Sun, 02 Feb 2020 19:49:33 GMT  
		Size: 57.2 MB (57190715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac7f8eecf6e47209978b8484171c538983fd231a5a833b0b3a7d4e8975d3411`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; 386

```console
$ docker pull redmine@sha256:0fb7c16c6ed2458c52ade08fcc7aee843a838ef7d90da9d98d4b4501a83fdd28
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220910454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69331927d39ab8ede3ae82a7009bdd1d19a8f90f6aa5e7807c4387dbcacd51a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 09:52:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 09:52:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 09:52:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 09:52:15 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:14:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:15:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:15:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:15:23 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:15:24 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:15:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:15:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 13:15:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 13:15:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:17:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:17:59 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:17:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:18:00 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:18:00 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e5d604e111de701bacf8c6952c8658d23d38b32c40a699c9ffdd0a50c9f45`  
		Last Modified: Sun, 02 Feb 2020 10:40:28 GMT  
		Size: 20.9 MB (20885510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640ed0b4362227a298cdba0f568b4516440d1041650eed93add06c421dec473`  
		Last Modified: Sun, 02 Feb 2020 10:40:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ba87587e473025c53ccdc291f0ff3cb00d050037298dbbf09bea4e9a96e273`  
		Last Modified: Sun, 02 Feb 2020 13:28:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d1e5b965a8e946b00d9e203d026eebcea799c872e86aab10892b19a25573e1`  
		Last Modified: Sun, 02 Feb 2020 13:28:53 GMT  
		Size: 94.7 MB (94691964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7823a2f443dfa05bc739245b9e6562ed6ce736eab799b6ab47ced9d157ec68`  
		Last Modified: Sun, 02 Feb 2020 13:28:07 GMT  
		Size: 1.3 MB (1275381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5977e8eed0d5080afd68d86e283b526522639b7d238c53aa3c350446da6e0496`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8464fc08c66d5812b90b3ec3186df531b6e99fb17df90d61454d428340e781d2`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4688da52009d0f4d4436d254808e6b9dcd304a95222fa3ac1611d00225809182`  
		Last Modified: Sun, 02 Feb 2020 13:28:08 GMT  
		Size: 2.7 MB (2735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f56b39600309d764a728a6af38afc43b71852287e8236e74ca5eac034a1c5`  
		Last Modified: Sun, 02 Feb 2020 13:28:28 GMT  
		Size: 56.4 MB (56364790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09d36e70af01f3cd70a01df4e6d5949d56fe641d8d895fcc242c91f75451e4e`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; ppc64le

```console
$ docker pull redmine@sha256:65f7bee1e807535980a5d3a2a6faf187e1f706da092dc09b923e4b11b041f930
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227251848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceee0df6cf0aa3c88905cdf9aba7438a919d629c7e66e784521ef17b3204d2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:21:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:24:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:24:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:24:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:24:26 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:24:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:24:34 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 16:24:36 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 16:24:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:28:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:28:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:28:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:28:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:28:27 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:28:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da40f6ba93d0a415759b121cffd59a714d0f9c8ea1c9ae9399dfd8ee2ba0a49c`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba55cb767e55fbec8edc12b9b116d3fd5959e82478ad073aa4c16b21ed5fe9`  
		Last Modified: Sun, 02 Feb 2020 16:53:06 GMT  
		Size: 100.3 MB (100283339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aac9fe590c395f90d840a0b6f490cb158a13321b799e4994a1bd1514d25eef`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.2 MB (1232443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97021c4ffbeff7d0d7e315631e4eb080205367e8997876c04d80d02271b6e38`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207503016878e07ef9be87106c3f4a0b46ad75c6f65c9ac0bc9c33ab6af9f34a`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e246ddcfdcc8d1ac853928cfed7c2d2e591666b1afe656a637c3b1ea14e7e7e`  
		Last Modified: Sun, 02 Feb 2020 16:52:40 GMT  
		Size: 2.7 MB (2735859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac7132221ca2c54eae8b8ee34564de1198fe84a573e709c1c589cf6d02cca5`  
		Last Modified: Sun, 02 Feb 2020 16:52:48 GMT  
		Size: 57.8 MB (57820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5915d8cf49b43d9212479a3fa1d53b6f44892c808bddf15679344b9ba445851`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; s390x

```console
$ docker pull redmine@sha256:ab1568d6b226e18d614f69224ab5082f76ab6c3c459575b451c0b43a044e4c88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210607230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e81bbd4d53db9fe58b1f99028cbe990f74848ac4052582c07576953e60742dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_MAJOR=2.6
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_VERSION=2.6.5
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sat, 01 Feb 2020 22:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:36:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:36:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:36:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:24:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:25:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:25:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:25:35 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:25:36 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 03:25:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:28:15 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:28:15 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:28:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:28:16 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:28:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f50ba1593f8ab66d1deaf12e190c35ecfea96815beda37efe10f1246f342b`  
		Last Modified: Sat, 01 Feb 2020 22:57:18 GMT  
		Size: 21.6 MB (21592569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a5d1fd225888733445fbc5a03464b232ab7c659a3bf619e93c5670a0ca594`  
		Last Modified: Sat, 01 Feb 2020 22:57:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6b52758f305e2a6eca340f3801ffcd699d9f9863ebfe870573fbea05f125b`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b9c2d954e677f77134627d444d4526d3dd757e20731a3db791ee045bd3ff5`  
		Last Modified: Sun, 02 Feb 2020 03:35:13 GMT  
		Size: 90.8 MB (90810821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4b03bbe680823684e8167d23322040275fc82bb40b38251bd1aca1d9759997`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.3 MB (1297549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a56833da980d550b03c0656e63d42b60190fa8f5b743d0efd1679e03cb5ea`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6743cd35c07b27ae19792d6c94243798a11247fa7a5f0fd8d63ec5fec7f8c8`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0844cdbf926f537d20bc1295376495cb2b126746d549e3cc88402e855e2f92`  
		Last Modified: Sun, 02 Feb 2020 03:34:58 GMT  
		Size: 2.7 MB (2735858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0c8052dd4f2d2e8e61136ca875e5667f9fdd869156f21339a352533be465b`  
		Last Modified: Sun, 02 Feb 2020 03:35:25 GMT  
		Size: 57.7 MB (57664549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b47a626d921e859c5def90095c9624aa612e063bcacdce5bb5485574308e28`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.0`

```console
$ docker pull redmine@sha256:2b80a2f231e0c3151048b900e06e2f1188e6c48a6d67fa57666498d6d3e11d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.1.0` - linux; amd64

```console
$ docker pull redmine@sha256:41c835c5d62a566e3205ec0de8b69a0d7ba82ab92db3f2c6f6f694079a39ce7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215447934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd730be099a4d92ac9ece41b026c8a9eeb9bbce1391737a3b27a2a7a5c96fb10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.0` - linux; arm variant v5

```console
$ docker pull redmine@sha256:d81487b3c1ad872dcf937922c70e1b33aa56ba4ce5190286fa2d86d8adeedc35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204856480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb08d7d0f07498236e41fdcf83db177fea39c1c452b01cf798acd1a6878621b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:16:09 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 02:16:12 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 02:16:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 02:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 02:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 02:19:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 02:20:03 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:44:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:46:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:46:22 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 09:46:22 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 09:46:23 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 09:46:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 09:46:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 09:46:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 09:46:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 09:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:50:23 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 09:50:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 09:50:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 09:50:25 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 09:50:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdd05ffdd7888092a6ef03be377963c297edec0344ce762bb6b3e1e2f114b94`  
		Last Modified: Sun, 02 Feb 2020 03:16:40 GMT  
		Size: 20.7 MB (20712712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e99c39d252f8cf22fae4749b2764aec83374848c63b8546989494f7f7a1cd2`  
		Last Modified: Sun, 02 Feb 2020 03:16:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff532b6c7852f386bab467c7b3f4b83b928ea314de236796805380d538c9717`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2386bd4b4f50f1d8f93b32303170d0866887841332213e58a371ca1bb7a20589`  
		Last Modified: Sun, 02 Feb 2020 10:07:52 GMT  
		Size: 88.7 MB (88656018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3116bbee905e3f17958856da579a4d33255abeddc081a9673f7e7751b098ebe`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.3 MB (1265374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a450151953d1dd4bd9521617998e60400bbde5af211dc4477b78be4b3f12675b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98603c054417f4f97943b58f87a4064bff0a6fdcc842f801c987da619b29ff3b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23326958468d4e64c292656ee80e58902c0ffdb4d9dd0ebe0f3ab5264ce8d22`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 2.7 MB (2735847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb53308614fca2cb01c7b7851bffaab106d45dee36ec93f25b881241ff56a0`  
		Last Modified: Sun, 02 Feb 2020 10:07:31 GMT  
		Size: 56.3 MB (56326279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2affc3b6a6c7eac6ca68be7e12a92c5998344deee6abc0a859b5698bb25dfdcc`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.0` - linux; arm variant v7

```console
$ docker pull redmine@sha256:9e0f94008f8a2c500a8c924488a7529a4a1c3ec8ed88647c3dccdb05eb336cfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20602d68bea242b9e0df73f8c1cb3ec695ca48e7b2d34ca2193d1e41d38a76d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 03:44:54 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 03:44:55 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 03:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 03:49:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:49:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:49:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:49:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:23:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:24:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:24:56 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:24:57 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:24:57 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:25:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 18:25:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:28:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:28:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:28:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:28:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:28:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:28:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fb6d3f67479293696c0ab1862f3d3cc1ccc4c655c60fe8a6b96d3958a13be`  
		Last Modified: Sun, 02 Feb 2020 04:38:21 GMT  
		Size: 20.6 MB (20620356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b57ca0c1f7b3cf1cf1382ec1048a03d8dd1fdd32b795c902f5305133d27c78`  
		Last Modified: Sun, 02 Feb 2020 04:38:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7e084272859dee62cdf07109bf3e8805638cf379acc552cbe57103d7127d7`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acdfe876f23507df2a4699b62233e5db893da68e0714670b2969ef99c3e4a85`  
		Last Modified: Sun, 02 Feb 2020 18:42:40 GMT  
		Size: 84.7 MB (84707975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4870f608fea5ec1df650afdeb0c7cac2ba24338f4ed4869ec1edf65dc3fa0c10`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.3 MB (1258130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cc28beecc94c51bb3c2e9bba9085acdb45f0cf6597ddba6286a4bc6244615`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0de6c18a6248274446744a98c3073bd3b138523d0975cc79e90fd546a2347`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1f3d8cad218ec457642439ef0e21e35b559965647074943fc07db7dafb8743`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 2.7 MB (2735837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcaa8a3e3e84f31845a917fd61aad8eb9520cc340d01f508f4506549341c5b4`  
		Last Modified: Sun, 02 Feb 2020 18:42:22 GMT  
		Size: 56.1 MB (56088174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b64e249084f0b4a1d8e939df4443bff48c435a17efb9d45dbc395d6444a984`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.0` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:46f7558e68186926a79a1f9eefe59f70dabee4e16f3e1bd4ef81f04306c34965
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211195925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31550a4fb8bf9ac5cca4bef14798e52e08b79e17ed4b36c9836b2c07eb42992`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 10:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 10:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:09:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:09:34 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:31:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:32:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:32:45 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:32:46 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:32:46 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:32:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:32:48 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 19:32:49 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 19:32:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:36:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:36:05 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:36:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:36:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:36:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:36:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e033592aeac21c0ce386b8333f16f6235250b4a12589032d45952f28aae99`  
		Last Modified: Sun, 02 Feb 2020 10:58:31 GMT  
		Size: 21.3 MB (21281648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb4967683b60ada551e77eafdd485daad99a6f1942cf491c5976877e6a7ca01`  
		Last Modified: Sun, 02 Feb 2020 10:58:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1923f0191bb3e7f14a51e3b4eeeb28deece511d37ce6f497c40bda83f1465`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154e1dcb614be456b08a22da421f1470ea51295943e88b2a0eada860e5585180`  
		Last Modified: Sun, 02 Feb 2020 19:49:49 GMT  
		Size: 91.6 MB (91645303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6070fa62d6076ace9b5fdbbc4425f553159ca73742af8b61b21c7cc62e28dc5b`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.2 MB (1242753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9b86ab04e3610da622ab684cf5116bb375dc072d2904d889e41ad6446aa3a9`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6d1aea2f7bdeae18fdbd703e35ea9ccadf83021960b2e8910c5c9a409e4d31`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade23107ce3d3cfd24a6e9442e7c716423ce08ab6e9554e2a3a54deb2cdca4f`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 2.7 MB (2735843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31458ee540982d7eea52baa93517c1a913991aac9330899a1fdf3bc869f11d`  
		Last Modified: Sun, 02 Feb 2020 19:49:33 GMT  
		Size: 57.2 MB (57190715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac7f8eecf6e47209978b8484171c538983fd231a5a833b0b3a7d4e8975d3411`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.0` - linux; 386

```console
$ docker pull redmine@sha256:0fb7c16c6ed2458c52ade08fcc7aee843a838ef7d90da9d98d4b4501a83fdd28
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220910454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69331927d39ab8ede3ae82a7009bdd1d19a8f90f6aa5e7807c4387dbcacd51a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 09:52:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 09:52:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 09:52:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 09:52:15 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:14:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:15:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:15:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:15:23 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:15:24 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:15:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:15:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 13:15:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 13:15:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:17:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:17:59 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:17:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:18:00 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:18:00 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e5d604e111de701bacf8c6952c8658d23d38b32c40a699c9ffdd0a50c9f45`  
		Last Modified: Sun, 02 Feb 2020 10:40:28 GMT  
		Size: 20.9 MB (20885510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640ed0b4362227a298cdba0f568b4516440d1041650eed93add06c421dec473`  
		Last Modified: Sun, 02 Feb 2020 10:40:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ba87587e473025c53ccdc291f0ff3cb00d050037298dbbf09bea4e9a96e273`  
		Last Modified: Sun, 02 Feb 2020 13:28:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d1e5b965a8e946b00d9e203d026eebcea799c872e86aab10892b19a25573e1`  
		Last Modified: Sun, 02 Feb 2020 13:28:53 GMT  
		Size: 94.7 MB (94691964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7823a2f443dfa05bc739245b9e6562ed6ce736eab799b6ab47ced9d157ec68`  
		Last Modified: Sun, 02 Feb 2020 13:28:07 GMT  
		Size: 1.3 MB (1275381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5977e8eed0d5080afd68d86e283b526522639b7d238c53aa3c350446da6e0496`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8464fc08c66d5812b90b3ec3186df531b6e99fb17df90d61454d428340e781d2`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4688da52009d0f4d4436d254808e6b9dcd304a95222fa3ac1611d00225809182`  
		Last Modified: Sun, 02 Feb 2020 13:28:08 GMT  
		Size: 2.7 MB (2735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f56b39600309d764a728a6af38afc43b71852287e8236e74ca5eac034a1c5`  
		Last Modified: Sun, 02 Feb 2020 13:28:28 GMT  
		Size: 56.4 MB (56364790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09d36e70af01f3cd70a01df4e6d5949d56fe641d8d895fcc242c91f75451e4e`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.0` - linux; ppc64le

```console
$ docker pull redmine@sha256:65f7bee1e807535980a5d3a2a6faf187e1f706da092dc09b923e4b11b041f930
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227251848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceee0df6cf0aa3c88905cdf9aba7438a919d629c7e66e784521ef17b3204d2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:21:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:24:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:24:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:24:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:24:26 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:24:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:24:34 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 16:24:36 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 16:24:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:28:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:28:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:28:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:28:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:28:27 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:28:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da40f6ba93d0a415759b121cffd59a714d0f9c8ea1c9ae9399dfd8ee2ba0a49c`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba55cb767e55fbec8edc12b9b116d3fd5959e82478ad073aa4c16b21ed5fe9`  
		Last Modified: Sun, 02 Feb 2020 16:53:06 GMT  
		Size: 100.3 MB (100283339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aac9fe590c395f90d840a0b6f490cb158a13321b799e4994a1bd1514d25eef`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.2 MB (1232443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97021c4ffbeff7d0d7e315631e4eb080205367e8997876c04d80d02271b6e38`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207503016878e07ef9be87106c3f4a0b46ad75c6f65c9ac0bc9c33ab6af9f34a`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e246ddcfdcc8d1ac853928cfed7c2d2e591666b1afe656a637c3b1ea14e7e7e`  
		Last Modified: Sun, 02 Feb 2020 16:52:40 GMT  
		Size: 2.7 MB (2735859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac7132221ca2c54eae8b8ee34564de1198fe84a573e709c1c589cf6d02cca5`  
		Last Modified: Sun, 02 Feb 2020 16:52:48 GMT  
		Size: 57.8 MB (57820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5915d8cf49b43d9212479a3fa1d53b6f44892c808bddf15679344b9ba445851`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.0` - linux; s390x

```console
$ docker pull redmine@sha256:ab1568d6b226e18d614f69224ab5082f76ab6c3c459575b451c0b43a044e4c88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210607230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e81bbd4d53db9fe58b1f99028cbe990f74848ac4052582c07576953e60742dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_MAJOR=2.6
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_VERSION=2.6.5
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sat, 01 Feb 2020 22:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:36:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:36:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:36:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:24:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:25:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:25:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:25:35 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:25:36 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 03:25:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:28:15 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:28:15 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:28:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:28:16 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:28:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f50ba1593f8ab66d1deaf12e190c35ecfea96815beda37efe10f1246f342b`  
		Last Modified: Sat, 01 Feb 2020 22:57:18 GMT  
		Size: 21.6 MB (21592569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a5d1fd225888733445fbc5a03464b232ab7c659a3bf619e93c5670a0ca594`  
		Last Modified: Sat, 01 Feb 2020 22:57:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6b52758f305e2a6eca340f3801ffcd699d9f9863ebfe870573fbea05f125b`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b9c2d954e677f77134627d444d4526d3dd757e20731a3db791ee045bd3ff5`  
		Last Modified: Sun, 02 Feb 2020 03:35:13 GMT  
		Size: 90.8 MB (90810821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4b03bbe680823684e8167d23322040275fc82bb40b38251bd1aca1d9759997`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.3 MB (1297549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a56833da980d550b03c0656e63d42b60190fa8f5b743d0efd1679e03cb5ea`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6743cd35c07b27ae19792d6c94243798a11247fa7a5f0fd8d63ec5fec7f8c8`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0844cdbf926f537d20bc1295376495cb2b126746d549e3cc88402e855e2f92`  
		Last Modified: Sun, 02 Feb 2020 03:34:58 GMT  
		Size: 2.7 MB (2735858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0c8052dd4f2d2e8e61136ca875e5667f9fdd869156f21339a352533be465b`  
		Last Modified: Sun, 02 Feb 2020 03:35:25 GMT  
		Size: 57.7 MB (57664549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b47a626d921e859c5def90095c9624aa612e063bcacdce5bb5485574308e28`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.0-alpine`

```console
$ docker pull redmine@sha256:4cf27b467b7efee154bf1200b03925094dcbee0d8db708c2c1ddf5587ef8a0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1.0-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:8dca5e32e3f4f1b74e2d3b12ee4509223694f6c35c80a35b462350f530e418d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152675939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aea4d9afbc8b24ba2b8683642b3634cb4af5a361967bf5da6fcafaa4ae3a439`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_VERSION=2.6.5
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Thu, 23 Jan 2020 22:54:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:55:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 22:55:00 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:20:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 25 Jan 2020 03:02:42 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 25 Jan 2020 03:02:42 GMT
ENV RAILS_ENV=production
# Sat, 25 Jan 2020 03:02:42 GMT
WORKDIR /usr/src/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
ENV HOME=/home/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 25 Jan 2020 03:02:43 GMT
ENV REDMINE_VERSION=4.1.0
# Sat, 25 Jan 2020 03:02:44 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sat, 25 Jan 2020 03:02:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:04:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:04:24 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:04:25 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:04:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:04:25 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:04:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058dc40fe23d25b2a6b8b9a31a6064c2eac5b373f52d5acb6d9219394f18a6c`  
		Last Modified: Thu, 23 Jan 2020 23:08:01 GMT  
		Size: 22.1 MB (22078401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabe7657d0e85ffedf267cb47d1b5a01f8da1f182f429defe848b0cdb2233ab1`  
		Last Modified: Thu, 23 Jan 2020 23:07:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a8cf67746eef043d81238dcc09e82c7404ac11ded1b543a0d44ef4b43b1f6f`  
		Last Modified: Fri, 24 Jan 2020 15:26:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568aba8514f204b93c18b8eaa4a6a10b1dc92d352b0bfc41cdb4fd157b88d21a`  
		Last Modified: Sat, 25 Jan 2020 03:15:53 GMT  
		Size: 67.8 MB (67774141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dacea602a3aaea9db5b6718ed6f84d15bb2efed2ac2e05bef99abf6569720d1`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dec2fc3052aebbbdb9c6a1a67e059e213b5e5c7c810d9595b33c2f3f342cf2`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6ae9955e302f74f4c9316777133885c5bf958ed173d65759757c8ec5851934`  
		Last Modified: Sat, 25 Jan 2020 03:15:39 GMT  
		Size: 2.7 MB (2736232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296d0c68ebdb2f40e192360f52529db01ea6473b1fc893aced2659b3e4d102d`  
		Last Modified: Sat, 25 Jan 2020 03:15:47 GMT  
		Size: 56.3 MB (56266046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd7ae63629d03f592f27e8117eaae2d70ee2380134b5581049703258b91339`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.0-passenger`

```console
$ docker pull redmine@sha256:0cb15d748d56fc48609b1c6ca59fbac8224a352e7139ac099c9358e299422abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1.0-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:59d4c410480712f1d07ca08c4e0345feb58ba1a1dfb467e915d5ff013ce9b401
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240300829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e581e9c6ccbd959e8c3a11ccf8f4a756e5fc137c4e7128a6e7bc215a2c8c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:07:15 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:07:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:33 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:07:33 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:07:33 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5c80ba374cc300e6e142b877569d9bc64884c6ca35096d99e42aec3574386`  
		Last Modified: Sun, 02 Feb 2020 23:15:11 GMT  
		Size: 19.9 MB (19935055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9617a5ab10a172b258cdb5194506b0e5f76683110bc8af86277faaca81d0f`  
		Last Modified: Sun, 02 Feb 2020 23:15:09 GMT  
		Size: 4.9 MB (4917840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-alpine`

```console
$ docker pull redmine@sha256:4cf27b467b7efee154bf1200b03925094dcbee0d8db708c2c1ddf5587ef8a0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:8dca5e32e3f4f1b74e2d3b12ee4509223694f6c35c80a35b462350f530e418d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152675939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aea4d9afbc8b24ba2b8683642b3634cb4af5a361967bf5da6fcafaa4ae3a439`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_VERSION=2.6.5
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Thu, 23 Jan 2020 22:54:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:55:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 22:55:00 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:20:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 25 Jan 2020 03:02:42 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 25 Jan 2020 03:02:42 GMT
ENV RAILS_ENV=production
# Sat, 25 Jan 2020 03:02:42 GMT
WORKDIR /usr/src/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
ENV HOME=/home/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 25 Jan 2020 03:02:43 GMT
ENV REDMINE_VERSION=4.1.0
# Sat, 25 Jan 2020 03:02:44 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sat, 25 Jan 2020 03:02:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:04:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:04:24 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:04:25 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:04:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:04:25 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:04:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058dc40fe23d25b2a6b8b9a31a6064c2eac5b373f52d5acb6d9219394f18a6c`  
		Last Modified: Thu, 23 Jan 2020 23:08:01 GMT  
		Size: 22.1 MB (22078401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabe7657d0e85ffedf267cb47d1b5a01f8da1f182f429defe848b0cdb2233ab1`  
		Last Modified: Thu, 23 Jan 2020 23:07:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a8cf67746eef043d81238dcc09e82c7404ac11ded1b543a0d44ef4b43b1f6f`  
		Last Modified: Fri, 24 Jan 2020 15:26:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568aba8514f204b93c18b8eaa4a6a10b1dc92d352b0bfc41cdb4fd157b88d21a`  
		Last Modified: Sat, 25 Jan 2020 03:15:53 GMT  
		Size: 67.8 MB (67774141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dacea602a3aaea9db5b6718ed6f84d15bb2efed2ac2e05bef99abf6569720d1`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dec2fc3052aebbbdb9c6a1a67e059e213b5e5c7c810d9595b33c2f3f342cf2`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6ae9955e302f74f4c9316777133885c5bf958ed173d65759757c8ec5851934`  
		Last Modified: Sat, 25 Jan 2020 03:15:39 GMT  
		Size: 2.7 MB (2736232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296d0c68ebdb2f40e192360f52529db01ea6473b1fc893aced2659b3e4d102d`  
		Last Modified: Sat, 25 Jan 2020 03:15:47 GMT  
		Size: 56.3 MB (56266046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd7ae63629d03f592f27e8117eaae2d70ee2380134b5581049703258b91339`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-passenger`

```console
$ docker pull redmine@sha256:0cb15d748d56fc48609b1c6ca59fbac8224a352e7139ac099c9358e299422abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4.1-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:59d4c410480712f1d07ca08c4e0345feb58ba1a1dfb467e915d5ff013ce9b401
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240300829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e581e9c6ccbd959e8c3a11ccf8f4a756e5fc137c4e7128a6e7bc215a2c8c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:07:15 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:07:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:33 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:07:33 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:07:33 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5c80ba374cc300e6e142b877569d9bc64884c6ca35096d99e42aec3574386`  
		Last Modified: Sun, 02 Feb 2020 23:15:11 GMT  
		Size: 19.9 MB (19935055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9617a5ab10a172b258cdb5194506b0e5f76683110bc8af86277faaca81d0f`  
		Last Modified: Sun, 02 Feb 2020 23:15:09 GMT  
		Size: 4.9 MB (4917840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:4cf27b467b7efee154bf1200b03925094dcbee0d8db708c2c1ddf5587ef8a0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:8dca5e32e3f4f1b74e2d3b12ee4509223694f6c35c80a35b462350f530e418d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152675939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aea4d9afbc8b24ba2b8683642b3634cb4af5a361967bf5da6fcafaa4ae3a439`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_VERSION=2.6.5
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Thu, 23 Jan 2020 22:54:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:55:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 22:55:00 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:20:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 25 Jan 2020 03:02:42 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 25 Jan 2020 03:02:42 GMT
ENV RAILS_ENV=production
# Sat, 25 Jan 2020 03:02:42 GMT
WORKDIR /usr/src/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
ENV HOME=/home/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 25 Jan 2020 03:02:43 GMT
ENV REDMINE_VERSION=4.1.0
# Sat, 25 Jan 2020 03:02:44 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sat, 25 Jan 2020 03:02:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:04:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:04:24 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:04:25 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:04:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:04:25 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:04:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058dc40fe23d25b2a6b8b9a31a6064c2eac5b373f52d5acb6d9219394f18a6c`  
		Last Modified: Thu, 23 Jan 2020 23:08:01 GMT  
		Size: 22.1 MB (22078401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabe7657d0e85ffedf267cb47d1b5a01f8da1f182f429defe848b0cdb2233ab1`  
		Last Modified: Thu, 23 Jan 2020 23:07:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a8cf67746eef043d81238dcc09e82c7404ac11ded1b543a0d44ef4b43b1f6f`  
		Last Modified: Fri, 24 Jan 2020 15:26:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568aba8514f204b93c18b8eaa4a6a10b1dc92d352b0bfc41cdb4fd157b88d21a`  
		Last Modified: Sat, 25 Jan 2020 03:15:53 GMT  
		Size: 67.8 MB (67774141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dacea602a3aaea9db5b6718ed6f84d15bb2efed2ac2e05bef99abf6569720d1`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dec2fc3052aebbbdb9c6a1a67e059e213b5e5c7c810d9595b33c2f3f342cf2`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6ae9955e302f74f4c9316777133885c5bf958ed173d65759757c8ec5851934`  
		Last Modified: Sat, 25 Jan 2020 03:15:39 GMT  
		Size: 2.7 MB (2736232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296d0c68ebdb2f40e192360f52529db01ea6473b1fc893aced2659b3e4d102d`  
		Last Modified: Sat, 25 Jan 2020 03:15:47 GMT  
		Size: 56.3 MB (56266046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd7ae63629d03f592f27e8117eaae2d70ee2380134b5581049703258b91339`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:0cb15d748d56fc48609b1c6ca59fbac8224a352e7139ac099c9358e299422abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:59d4c410480712f1d07ca08c4e0345feb58ba1a1dfb467e915d5ff013ce9b401
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240300829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e581e9c6ccbd959e8c3a11ccf8f4a756e5fc137c4e7128a6e7bc215a2c8c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:07:15 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:07:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:33 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:07:33 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:07:33 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5c80ba374cc300e6e142b877569d9bc64884c6ca35096d99e42aec3574386`  
		Last Modified: Sun, 02 Feb 2020 23:15:11 GMT  
		Size: 19.9 MB (19935055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9617a5ab10a172b258cdb5194506b0e5f76683110bc8af86277faaca81d0f`  
		Last Modified: Sun, 02 Feb 2020 23:15:09 GMT  
		Size: 4.9 MB (4917840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:alpine`

```console
$ docker pull redmine@sha256:4cf27b467b7efee154bf1200b03925094dcbee0d8db708c2c1ddf5587ef8a0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:8dca5e32e3f4f1b74e2d3b12ee4509223694f6c35c80a35b462350f530e418d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152675939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aea4d9afbc8b24ba2b8683642b3634cb4af5a361967bf5da6fcafaa4ae3a439`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:45:09 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 23 Jan 2020 22:45:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_VERSION=2.6.5
# Thu, 23 Jan 2020 22:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Thu, 23 Jan 2020 22:54:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Jan 2020 22:54:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Jan 2020 22:54:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:55:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Jan 2020 22:55:00 GMT
CMD ["irb"]
# Fri, 24 Jan 2020 15:20:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 25 Jan 2020 03:02:42 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 25 Jan 2020 03:02:42 GMT
ENV RAILS_ENV=production
# Sat, 25 Jan 2020 03:02:42 GMT
WORKDIR /usr/src/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
ENV HOME=/home/redmine
# Sat, 25 Jan 2020 03:02:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 25 Jan 2020 03:02:43 GMT
ENV REDMINE_VERSION=4.1.0
# Sat, 25 Jan 2020 03:02:44 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sat, 25 Jan 2020 03:02:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 25 Jan 2020 03:04:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		su-exec redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 25 Jan 2020 03:04:24 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 25 Jan 2020 03:04:25 GMT
COPY file:74f57a1bf0a912dc2879462a72c1d654c2450fd1e1dad78bffaafda2974d3e97 in / 
# Sat, 25 Jan 2020 03:04:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 25 Jan 2020 03:04:25 GMT
EXPOSE 3000
# Sat, 25 Jan 2020 03:04:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b33ddc14734d2336fc9bef7d13319b166f5c65e02d4f0ea6bbbf42d29f1b8`  
		Last Modified: Thu, 23 Jan 2020 23:07:19 GMT  
		Size: 1.0 MB (1030290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbca8ca4a5960f56ab9c9b51eee7735d8bfeace0c8683b13e23d834e20e8898c`  
		Last Modified: Thu, 23 Jan 2020 23:07:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058dc40fe23d25b2a6b8b9a31a6064c2eac5b373f52d5acb6d9219394f18a6c`  
		Last Modified: Thu, 23 Jan 2020 23:08:01 GMT  
		Size: 22.1 MB (22078401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabe7657d0e85ffedf267cb47d1b5a01f8da1f182f429defe848b0cdb2233ab1`  
		Last Modified: Thu, 23 Jan 2020 23:07:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a8cf67746eef043d81238dcc09e82c7404ac11ded1b543a0d44ef4b43b1f6f`  
		Last Modified: Fri, 24 Jan 2020 15:26:52 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568aba8514f204b93c18b8eaa4a6a10b1dc92d352b0bfc41cdb4fd157b88d21a`  
		Last Modified: Sat, 25 Jan 2020 03:15:53 GMT  
		Size: 67.8 MB (67774141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dacea602a3aaea9db5b6718ed6f84d15bb2efed2ac2e05bef99abf6569720d1`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dec2fc3052aebbbdb9c6a1a67e059e213b5e5c7c810d9595b33c2f3f342cf2`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6ae9955e302f74f4c9316777133885c5bf958ed173d65759757c8ec5851934`  
		Last Modified: Sat, 25 Jan 2020 03:15:39 GMT  
		Size: 2.7 MB (2736232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296d0c68ebdb2f40e192360f52529db01ea6473b1fc893aced2659b3e4d102d`  
		Last Modified: Sat, 25 Jan 2020 03:15:47 GMT  
		Size: 56.3 MB (56266046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfd7ae63629d03f592f27e8117eaae2d70ee2380134b5581049703258b91339`  
		Last Modified: Sat, 25 Jan 2020 03:15:38 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:2b80a2f231e0c3151048b900e06e2f1188e6c48a6d67fa57666498d6d3e11d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:41c835c5d62a566e3205ec0de8b69a0d7ba82ab92db3f2c6f6f694079a39ce7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215447934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd730be099a4d92ac9ece41b026c8a9eeb9bbce1391737a3b27a2a7a5c96fb10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:d81487b3c1ad872dcf937922c70e1b33aa56ba4ce5190286fa2d86d8adeedc35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204856480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb08d7d0f07498236e41fdcf83db177fea39c1c452b01cf798acd1a6878621b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 02:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:08:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 02:16:09 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 02:16:12 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 02:16:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 02:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 02:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 02:19:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 02:20:03 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 09:44:56 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 09:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:46:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:46:22 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 09:46:22 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 09:46:23 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 09:46:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 09:46:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 09:46:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 09:46:31 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 09:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:50:23 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 09:50:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 09:50:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 09:50:25 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 09:50:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb489e800f7f428b98c5f257bb143dc6d911d3b076c3d9e0940d04f0f2557c`  
		Last Modified: Sun, 02 Feb 2020 03:16:08 GMT  
		Size: 10.3 MB (10326074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddfcf800a56c64451730cbfd34ac7b3da09bfe974245010cf9db34bc74f681`  
		Last Modified: Sun, 02 Feb 2020 03:16:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdd05ffdd7888092a6ef03be377963c297edec0344ce762bb6b3e1e2f114b94`  
		Last Modified: Sun, 02 Feb 2020 03:16:40 GMT  
		Size: 20.7 MB (20712712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e99c39d252f8cf22fae4749b2764aec83374848c63b8546989494f7f7a1cd2`  
		Last Modified: Sun, 02 Feb 2020 03:16:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff532b6c7852f386bab467c7b3f4b83b928ea314de236796805380d538c9717`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2386bd4b4f50f1d8f93b32303170d0866887841332213e58a371ca1bb7a20589`  
		Last Modified: Sun, 02 Feb 2020 10:07:52 GMT  
		Size: 88.7 MB (88656018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3116bbee905e3f17958856da579a4d33255abeddc081a9673f7e7751b098ebe`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 1.3 MB (1265374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a450151953d1dd4bd9521617998e60400bbde5af211dc4477b78be4b3f12675b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98603c054417f4f97943b58f87a4064bff0a6fdcc842f801c987da619b29ff3b`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23326958468d4e64c292656ee80e58902c0ffdb4d9dd0ebe0f3ab5264ce8d22`  
		Last Modified: Sun, 02 Feb 2020 10:07:19 GMT  
		Size: 2.7 MB (2735847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb53308614fca2cb01c7b7851bffaab106d45dee36ec93f25b881241ff56a0`  
		Last Modified: Sun, 02 Feb 2020 10:07:31 GMT  
		Size: 56.3 MB (56326279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2affc3b6a6c7eac6ca68be7e12a92c5998344deee6abc0a859b5698bb25dfdcc`  
		Last Modified: Sun, 02 Feb 2020 10:07:17 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:9e0f94008f8a2c500a8c924488a7529a4a1c3ec8ed88647c3dccdb05eb336cfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20602d68bea242b9e0df73f8c1cb3ec695ca48e7b2d34ca2193d1e41d38a76d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:26:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 03:44:54 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 03:44:55 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 03:44:56 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 03:49:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 03:49:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 03:49:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 03:49:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 03:49:19 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 18:23:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 18:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:24:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:24:56 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 18:24:57 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 18:24:57 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 18:25:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 18:25:01 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 18:25:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 18:28:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 18:28:43 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 18:28:44 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 18:28:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:28:45 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 18:28:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4814dc35805320e4b9357cbbb08a16b2fdf6fb2cc515726d081a934c414ad`  
		Last Modified: Sun, 02 Feb 2020 04:37:50 GMT  
		Size: 9.8 MB (9847353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fe22250f5be96c8fee4c95a756bd855486de1468bbaab88889cb9a99919ce`  
		Last Modified: Sun, 02 Feb 2020 04:37:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fb6d3f67479293696c0ab1862f3d3cc1ccc4c655c60fe8a6b96d3958a13be`  
		Last Modified: Sun, 02 Feb 2020 04:38:21 GMT  
		Size: 20.6 MB (20620356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b57ca0c1f7b3cf1cf1382ec1048a03d8dd1fdd32b795c902f5305133d27c78`  
		Last Modified: Sun, 02 Feb 2020 04:38:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b7e084272859dee62cdf07109bf3e8805638cf379acc552cbe57103d7127d7`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acdfe876f23507df2a4699b62233e5db893da68e0714670b2969ef99c3e4a85`  
		Last Modified: Sun, 02 Feb 2020 18:42:40 GMT  
		Size: 84.7 MB (84707975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4870f608fea5ec1df650afdeb0c7cac2ba24338f4ed4869ec1edf65dc3fa0c10`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 1.3 MB (1258130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cc28beecc94c51bb3c2e9bba9085acdb45f0cf6597ddba6286a4bc6244615`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0de6c18a6248274446744a98c3073bd3b138523d0975cc79e90fd546a2347`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1f3d8cad218ec457642439ef0e21e35b559965647074943fc07db7dafb8743`  
		Last Modified: Sun, 02 Feb 2020 18:42:09 GMT  
		Size: 2.7 MB (2735837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcaa8a3e3e84f31845a917fd61aad8eb9520cc340d01f508f4506549341c5b4`  
		Last Modified: Sun, 02 Feb 2020 18:42:22 GMT  
		Size: 56.1 MB (56088174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b64e249084f0b4a1d8e939df4443bff48c435a17efb9d45dbc395d6444a984`  
		Last Modified: Sun, 02 Feb 2020 18:42:07 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:46f7558e68186926a79a1f9eefe59f70dabee4e16f3e1bd4ef81f04306c34965
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211195925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31550a4fb8bf9ac5cca4bef14798e52e08b79e17ed4b36c9836b2c07eb42992`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:57:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:57:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 10:05:44 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 10:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 10:09:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 10:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 10:09:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:09:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 10:09:34 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 19:31:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 19:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:32:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:32:45 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 19:32:46 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 19:32:46 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 19:32:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 19:32:48 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 19:32:49 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 19:32:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 19:36:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 19:36:05 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 19:36:05 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 19:36:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 19:36:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 19:36:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c2697ff6f058d7f0b17dfdf123fffce9a007b3f302b77c8b9bdc9fd7685d9`  
		Last Modified: Sun, 02 Feb 2020 10:58:01 GMT  
		Size: 11.2 MB (11244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783fe382da6383f2efde489fb27e5a517200e0b81cb49935ae0f0ce2a8d5e152`  
		Last Modified: Sun, 02 Feb 2020 10:57:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e033592aeac21c0ce386b8333f16f6235250b4a12589032d45952f28aae99`  
		Last Modified: Sun, 02 Feb 2020 10:58:31 GMT  
		Size: 21.3 MB (21281648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb4967683b60ada551e77eafdd485daad99a6f1942cf491c5976877e6a7ca01`  
		Last Modified: Sun, 02 Feb 2020 10:58:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d1923f0191bb3e7f14a51e3b4eeeb28deece511d37ce6f497c40bda83f1465`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154e1dcb614be456b08a22da421f1470ea51295943e88b2a0eada860e5585180`  
		Last Modified: Sun, 02 Feb 2020 19:49:49 GMT  
		Size: 91.6 MB (91645303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6070fa62d6076ace9b5fdbbc4425f553159ca73742af8b61b21c7cc62e28dc5b`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 1.2 MB (1242753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9b86ab04e3610da622ab684cf5116bb375dc072d2904d889e41ad6446aa3a9`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6d1aea2f7bdeae18fdbd703e35ea9ccadf83021960b2e8910c5c9a409e4d31`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade23107ce3d3cfd24a6e9442e7c716423ce08ab6e9554e2a3a54deb2cdca4f`  
		Last Modified: Sun, 02 Feb 2020 19:49:21 GMT  
		Size: 2.7 MB (2735843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31458ee540982d7eea52baa93517c1a913991aac9330899a1fdf3bc869f11d`  
		Last Modified: Sun, 02 Feb 2020 19:49:33 GMT  
		Size: 57.2 MB (57190715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac7f8eecf6e47209978b8484171c538983fd231a5a833b0b3a7d4e8975d3411`  
		Last Modified: Sun, 02 Feb 2020 19:49:19 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:0fb7c16c6ed2458c52ade08fcc7aee843a838ef7d90da9d98d4b4501a83fdd28
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220910454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69331927d39ab8ede3ae82a7009bdd1d19a8f90f6aa5e7807c4387dbcacd51a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 09:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 09:39:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 09:48:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 09:52:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 09:52:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 09:52:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 09:52:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 09:52:15 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 13:14:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 13:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 13:15:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:15:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 13:15:23 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 13:15:24 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 13:15:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 13:15:25 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 13:15:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 13:15:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 13:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 13:17:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 13:17:59 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 13:17:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 13:18:00 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 13:18:00 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd448d2713c41a4a7de819558285e075713444e2664f5e9180ae765e0168be4`  
		Last Modified: Sun, 02 Feb 2020 10:40:01 GMT  
		Size: 17.2 MB (17205970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44fb48efbb69a28436d9d68bf4e52520dc4f725a894f8e270181ce6fcb40ef`  
		Last Modified: Sun, 02 Feb 2020 10:39:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7e5d604e111de701bacf8c6952c8658d23d38b32c40a699c9ffdd0a50c9f45`  
		Last Modified: Sun, 02 Feb 2020 10:40:28 GMT  
		Size: 20.9 MB (20885510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5640ed0b4362227a298cdba0f568b4516440d1041650eed93add06c421dec473`  
		Last Modified: Sun, 02 Feb 2020 10:40:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ba87587e473025c53ccdc291f0ff3cb00d050037298dbbf09bea4e9a96e273`  
		Last Modified: Sun, 02 Feb 2020 13:28:06 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d1e5b965a8e946b00d9e203d026eebcea799c872e86aab10892b19a25573e1`  
		Last Modified: Sun, 02 Feb 2020 13:28:53 GMT  
		Size: 94.7 MB (94691964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7823a2f443dfa05bc739245b9e6562ed6ce736eab799b6ab47ced9d157ec68`  
		Last Modified: Sun, 02 Feb 2020 13:28:07 GMT  
		Size: 1.3 MB (1275381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5977e8eed0d5080afd68d86e283b526522639b7d238c53aa3c350446da6e0496`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8464fc08c66d5812b90b3ec3186df531b6e99fb17df90d61454d428340e781d2`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4688da52009d0f4d4436d254808e6b9dcd304a95222fa3ac1611d00225809182`  
		Last Modified: Sun, 02 Feb 2020 13:28:08 GMT  
		Size: 2.7 MB (2735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f56b39600309d764a728a6af38afc43b71852287e8236e74ca5eac034a1c5`  
		Last Modified: Sun, 02 Feb 2020 13:28:28 GMT  
		Size: 56.4 MB (56364790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09d36e70af01f3cd70a01df4e6d5949d56fe641d8d895fcc242c91f75451e4e`  
		Last Modified: Sun, 02 Feb 2020 13:28:04 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:65f7bee1e807535980a5d3a2a6faf187e1f706da092dc09b923e4b11b041f930
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227251848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceee0df6cf0aa3c88905cdf9aba7438a919d629c7e66e784521ef17b3204d2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:21:06 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 16:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:24:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:24:23 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 16:24:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 16:24:26 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 16:24:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 16:24:34 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 16:24:36 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 16:24:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 16:28:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 16:28:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 16:28:23 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 16:28:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:28:27 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 16:28:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da40f6ba93d0a415759b121cffd59a714d0f9c8ea1c9ae9399dfd8ee2ba0a49c`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba55cb767e55fbec8edc12b9b116d3fd5959e82478ad073aa4c16b21ed5fe9`  
		Last Modified: Sun, 02 Feb 2020 16:53:06 GMT  
		Size: 100.3 MB (100283339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aac9fe590c395f90d840a0b6f490cb158a13321b799e4994a1bd1514d25eef`  
		Last Modified: Sun, 02 Feb 2020 16:52:43 GMT  
		Size: 1.2 MB (1232443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97021c4ffbeff7d0d7e315631e4eb080205367e8997876c04d80d02271b6e38`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207503016878e07ef9be87106c3f4a0b46ad75c6f65c9ac0bc9c33ab6af9f34a`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e246ddcfdcc8d1ac853928cfed7c2d2e591666b1afe656a637c3b1ea14e7e7e`  
		Last Modified: Sun, 02 Feb 2020 16:52:40 GMT  
		Size: 2.7 MB (2735859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac7132221ca2c54eae8b8ee34564de1198fe84a573e709c1c589cf6d02cca5`  
		Last Modified: Sun, 02 Feb 2020 16:52:48 GMT  
		Size: 57.8 MB (57820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5915d8cf49b43d9212479a3fa1d53b6f44892c808bddf15679344b9ba445851`  
		Last Modified: Sun, 02 Feb 2020 16:52:38 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:ab1568d6b226e18d614f69224ab5082f76ab6c3c459575b451c0b43a044e4c88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210607230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e81bbd4d53db9fe58b1f99028cbe990f74848ac4052582c07576953e60742dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:29 GMT
ADD file:fb7d675adcb17ba15644d52683f50577e05e7e613dee00a1b2e40463f31bbf29 in / 
# Sat, 01 Feb 2020 16:42:30 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 22:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 22:24:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_MAJOR=2.6
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_VERSION=2.6.5
# Sat, 01 Feb 2020 22:34:36 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sat, 01 Feb 2020 22:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 01 Feb 2020 22:36:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 01 Feb 2020 22:36:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 22:36:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 01 Feb 2020 22:36:07 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 03:24:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 03:25:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 03:25:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:25:35 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 03:25:36 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 03:25:36 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 03:25:37 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 03:25:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 03:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:28:15 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 03:28:15 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 03:28:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 03:28:16 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 03:28:16 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:56a040772f0865ef22b9f53d560f9780e6aaa2ab7c117116a7832d97a10b06c1`  
		Last Modified: Sat, 01 Feb 2020 16:45:51 GMT  
		Size: 25.7 MB (25705378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17d8d1356b8293f168a2578ba81c34f07ee79d7a56bd579e776ad498d0b2e8`  
		Last Modified: Sat, 01 Feb 2020 22:56:51 GMT  
		Size: 10.8 MB (10795999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d180073499f34bb9340ecac840eeb00fab127188f731188ba78e76e435b62c`  
		Last Modified: Sat, 01 Feb 2020 22:56:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f50ba1593f8ab66d1deaf12e190c35ecfea96815beda37efe10f1246f342b`  
		Last Modified: Sat, 01 Feb 2020 22:57:18 GMT  
		Size: 21.6 MB (21592569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a5d1fd225888733445fbc5a03464b232ab7c659a3bf619e93c5670a0ca594`  
		Last Modified: Sat, 01 Feb 2020 22:57:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e6b52758f305e2a6eca340f3801ffcd699d9f9863ebfe870573fbea05f125b`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b9c2d954e677f77134627d444d4526d3dd757e20731a3db791ee045bd3ff5`  
		Last Modified: Sun, 02 Feb 2020 03:35:13 GMT  
		Size: 90.8 MB (90810821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4b03bbe680823684e8167d23322040275fc82bb40b38251bd1aca1d9759997`  
		Last Modified: Sun, 02 Feb 2020 03:34:59 GMT  
		Size: 1.3 MB (1297549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6a56833da980d550b03c0656e63d42b60190fa8f5b743d0efd1679e03cb5ea`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6743cd35c07b27ae19792d6c94243798a11247fa7a5f0fd8d63ec5fec7f8c8`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0844cdbf926f537d20bc1295376495cb2b126746d549e3cc88402e855e2f92`  
		Last Modified: Sun, 02 Feb 2020 03:34:58 GMT  
		Size: 2.7 MB (2735858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a0c8052dd4f2d2e8e61136ca875e5667f9fdd869156f21339a352533be465b`  
		Last Modified: Sun, 02 Feb 2020 03:35:25 GMT  
		Size: 57.7 MB (57664549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b47a626d921e859c5def90095c9624aa612e063bcacdce5bb5485574308e28`  
		Last Modified: Sun, 02 Feb 2020 03:34:57 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:0cb15d748d56fc48609b1c6ca59fbac8224a352e7139ac099c9358e299422abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:59d4c410480712f1d07ca08c4e0345feb58ba1a1dfb467e915d5ff013ce9b401
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240300829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e581e9c6ccbd959e8c3a11ccf8f4a756e5fc137c4e7128a6e7bc215a2c8c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:00:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:05 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:14:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:14:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:14:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:14:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:14:05 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 23:04:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 02 Feb 2020 23:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 23:05:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.11'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.18.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:05:25 GMT
ENV RAILS_ENV=production
# Sun, 02 Feb 2020 23:05:25 GMT
WORKDIR /usr/src/redmine
# Sun, 02 Feb 2020 23:05:25 GMT
ENV HOME=/home/redmine
# Sun, 02 Feb 2020 23:05:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_VERSION=4.1.0
# Sun, 02 Feb 2020 23:05:26 GMT
ENV REDMINE_DOWNLOAD_MD5=32c7b9ce4c419092da439b540cbc1dbf
# Sun, 02 Feb 2020 23:05:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_MD5 *redmine.tar.gz" | md5sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 02 Feb 2020 23:07:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		gosu redmine bundle install --jobs "$(nproc)" --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 02 Feb 2020 23:07:06 GMT
COPY file:df6d0160357b381a47abf010e78172591272c9029cb0436b6b6dfcc71483244e in / 
# Sun, 02 Feb 2020 23:07:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 23:07:07 GMT
EXPOSE 3000
# Sun, 02 Feb 2020 23:07:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Sun, 02 Feb 2020 23:07:15 GMT
ENV PASSENGER_VERSION=6.0.4
# Sun, 02 Feb 2020 23:07:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 23:07:33 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Sun, 02 Feb 2020 23:07:33 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Sun, 02 Feb 2020 23:07:33 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a21bafa1d6936db84e12efc3997df87e675a0b739b8db80eb433caa272efd93`  
		Last Modified: Sun, 02 Feb 2020 08:03:42 GMT  
		Size: 12.5 MB (12539741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689ccabb7d344598bdfcbe9cadcd9f0a5c56c53418e9a339e7d79637bc347da`  
		Last Modified: Sun, 02 Feb 2020 08:03:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daea10e1ee2bd87bc2acc2cb75d566eee0b2bb2c770a4a08291b8d55d03f7275`  
		Last Modified: Sun, 02 Feb 2020 08:04:00 GMT  
		Size: 21.4 MB (21445784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e47b5b29551b95b1f6773521490bcc87ec6dd573684b0b96f8c6dc6798e28`  
		Last Modified: Sun, 02 Feb 2020 08:03:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a48cf43437dc742390824bb02a83d5cc4c504bba1dcfb079fd944d7395ae7e`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54446116ccbd5f5e07d0f9e63f122ade623348acce3c43e408d674767146e547`  
		Last Modified: Sun, 02 Feb 2020 23:15:02 GMT  
		Size: 93.1 MB (93059144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e78d32e7eaf590082ee2b96975dcbe1f81ab46241c83ed55b63cd95cfcb3b79`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 1.3 MB (1307594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8ff5f09d85c1c19939487bd436e49a3d1e7b4250bfe44ae26b1974a6ac46e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e0b27aecb9055c5715b573d2ba7ecd3c3a2f637a25f7dbc1126b2c46f680e`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e997415b29ab4eb68ce0429abca97e9db0dc06d0bed2c0b8e02181c80aef190`  
		Last Modified: Sun, 02 Feb 2020 23:14:45 GMT  
		Size: 2.7 MB (2735384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d76cbc45da4b60f3d43aff75c856ca4daf984301f540b72ef391ecc72dfd7`  
		Last Modified: Sun, 02 Feb 2020 23:14:59 GMT  
		Size: 57.3 MB (57263624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30546c194a84d34d44ee5ccb631424b8156900ae0d847d8afdf8d5c184cf92`  
		Last Modified: Sun, 02 Feb 2020 23:14:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5c80ba374cc300e6e142b877569d9bc64884c6ca35096d99e42aec3574386`  
		Last Modified: Sun, 02 Feb 2020 23:15:11 GMT  
		Size: 19.9 MB (19935055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9617a5ab10a172b258cdb5194506b0e5f76683110bc8af86277faaca81d0f`  
		Last Modified: Sun, 02 Feb 2020 23:15:09 GMT  
		Size: 4.9 MB (4917840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
