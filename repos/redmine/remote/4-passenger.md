## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:119e8e8f0d6b720c03a097e802fea2faa7abbaf7218d13e122e9b3d082b95b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:22176ef80d36d7840b7a5c363902cfed9f1bed0203516c67eb17e0c157e1f049
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236798781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53791df92995762ce9dfad453ce2939a0f6e6b2709698cf9fb587c2ef07b94b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:57:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:58:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 31 Mar 2021 14:58:00 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 15:04:34 GMT
ENV RUBY_MAJOR=2.7
# Mon, 05 Apr 2021 19:12:20 GMT
ENV RUBY_VERSION=2.7.3
# Mon, 05 Apr 2021 19:12:21 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Mon, 05 Apr 2021 19:16:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 19:16:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 19:16:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 19:16:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 19:16:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 19:16:20 GMT
CMD ["irb"]
# Mon, 05 Apr 2021 20:42:15 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Mon, 05 Apr 2021 20:42:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 				shared-mime-info 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 05 Apr 2021 20:43:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		export GOSU_VERSION='1.12'; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		export TINI_VERSION='0.19.0'; 	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	gpgconf --kill all; 	rm -r "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini; 	tini -h; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 05 Apr 2021 20:43:17 GMT
ENV RAILS_ENV=production
# Mon, 05 Apr 2021 20:43:17 GMT
WORKDIR /usr/src/redmine
# Mon, 05 Apr 2021 20:43:17 GMT
ENV HOME=/home/redmine
# Mon, 05 Apr 2021 20:43:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 05 Apr 2021 20:43:19 GMT
ENV REDMINE_VERSION=4.2.0
# Mon, 05 Apr 2021 20:43:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=295864c580afa2a926e7a17f2ad10693f9b7a6d9f1ef523edb96b2368e7f07e5
# Mon, 05 Apr 2021 20:43:23 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 05 Apr 2021 20:44:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 05 Apr 2021 20:44:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 05 Apr 2021 20:44:11 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 05 Apr 2021 20:44:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Apr 2021 20:44:11 GMT
EXPOSE 3000
# Mon, 05 Apr 2021 20:44:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 05 Apr 2021 20:44:15 GMT
ENV PASSENGER_VERSION=6.0.8
# Mon, 05 Apr 2021 20:44:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 05 Apr 2021 20:44:34 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 05 Apr 2021 20:44:34 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 05 Apr 2021 20:44:34 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16df641547448e59edffbaa61470a9198c2a707bdb87082a5e5a06eba7f889e`  
		Last Modified: Wed, 31 Mar 2021 15:32:18 GMT  
		Size: 12.6 MB (12562281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc9849ece33d85b0a419e8eb0562951873d2dc0b12b30d06f1e7831b9d804ee`  
		Last Modified: Wed, 31 Mar 2021 15:32:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573ae2e6f30bad22dd93b6c8bfb1a07f0444597cd709afaa4bf905edb18874f5`  
		Last Modified: Mon, 05 Apr 2021 20:14:42 GMT  
		Size: 22.9 MB (22886645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f589d215145cf17518df4402efcd4eee9cdfa63a6ffbf4c9ed69f163616bd`  
		Last Modified: Mon, 05 Apr 2021 20:14:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0261aaa0397c84ea3e88a86878af27f5cf50b2ae348472b5bfb0e8d4f519ea99`  
		Last Modified: Mon, 05 Apr 2021 20:57:54 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa301b9330adeb0287b8bd73caeb2e81c30811b1f2057b660ad920aa0f122b`  
		Last Modified: Mon, 05 Apr 2021 20:58:10 GMT  
		Size: 93.9 MB (93905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600649d313246beb68d34e807c96388e543f2c5107c6a334a2d62a0edcb36418`  
		Last Modified: Mon, 05 Apr 2021 20:57:54 GMT  
		Size: 1.4 MB (1370327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f1fda98f04d5725bddfc9e14e00141aa289ac25dc44671175ecdb51d185782`  
		Last Modified: Mon, 05 Apr 2021 20:57:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e474f31363a0bbe2fbbc26feb9ed53d2647f79fc808c075627fc146cbd5ce25f`  
		Last Modified: Mon, 05 Apr 2021 20:57:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a158c69dc1679c661b938f2aee1e9f0c3db8206429d2681c5d1f2f02db60839`  
		Last Modified: Mon, 05 Apr 2021 20:57:52 GMT  
		Size: 3.1 MB (3057055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4030a0407d27dc3547eef0fb5b00d38abd3d87a25a37b257fe58b63217b9cf6f`  
		Last Modified: Mon, 05 Apr 2021 20:57:59 GMT  
		Size: 50.6 MB (50573399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785717cd9ae328720354bb53e24a29e89cda8bf1f7558fd3973abebf21ba72fe`  
		Last Modified: Mon, 05 Apr 2021 20:57:51 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb101b628d32298f0a53cc7c3d869f8ba478aa81ad52c1f636c45a3871bf31`  
		Last Modified: Mon, 05 Apr 2021 20:58:32 GMT  
		Size: 20.4 MB (20363252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc0308cde35823456054e19fe282c23c9924728680c2be9a652bcbae6576167`  
		Last Modified: Mon, 05 Apr 2021 20:58:30 GMT  
		Size: 4.9 MB (4936711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
